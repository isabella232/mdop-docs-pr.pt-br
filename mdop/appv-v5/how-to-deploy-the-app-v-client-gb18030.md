---
title: Como implantar o cliente do App-V
description: Como implantar o cliente do App-V
ms.author: dansimp
author: dansimp
ms.assetid: 9c4e67ae-ddaf-4e23-8c16-72d029a74a27
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/05/2018
ms.openlocfilehash: 4e246e13bf59f167eade77200afd866c6a3c41fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796420"
---
# Como implantar o cliente do App-V


Use o procedimento a seguir para instalar o cliente do Microsoft Application Virtualization (App-V) 5,0 e o cliente de serviços de área de trabalho remota. Você deve instalar a versão do cliente que corresponde ao sistema operacional do computador de destino.

<a href="" id="bkmk-clt-install-prereqs"></a>**O que fazer antes de começar**

1. Revise e instale os pré-requisitos do software:

   Instale o software obrigatório que corresponde à versão do App-V que você está instalando:

   - [Sobre o App-V 5.0 SP3](about-app-v-50-sp3.md)

   - App-V 5,0 SP1 e App-V 5,0 SP2 – não há novos pré-requisitos nessas versões

   - [Pré-requisitos do App-V 5.0](app-v-50-prerequisites.md)

2. Revise os cenários de coexistência e sem suporte do cliente, conforme aplicável à sua instalação:


   |                                               |                                                                                                                            |
   |-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
   |      Implantando clientes App-V coexistentes       | [Planejamento para a implantação do sequenciador e do cliente do App-V 5.0](planning-for-the-app-v-50-sequencer-and-client-deployment.md) |
   | Cenários de instalação sem suporte ou limitados |                         [Configurações com suporte ao App-V 5.0](app-v-50-supported-configurations.md)                         |

   ---

3. Examine os locais do registro do cliente, log e informações de solução de problemas:

#### Informações do registro do cliente
<ul><li>Por padrão, depois de instalar o cliente App-V 5,0, as informações do cliente são armazenadas no registro na seguinte chave do registro:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\APPV\CLIENT</code></li><li>Quando você implanta um pacote virtualizado em um computador que está executando o cliente App-V, os dados do pacote associado são armazenados no seguinte local:<p><p><code>C:\ProgramData\App-V</code><p><p>No entanto, você pode reconfigurar esse local com a seguinte chave do registro:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\SOFTWARE\MICROSOFT\APPV\CLIENT\STREAMING\PACKAGEINSTALLATIONROOT</code></li></ul>

#### Arquivos de log do cliente                  
<ul><li>Para informações do arquivo de log associadas ao cliente App-V 5,0, pesquise no seguinte log:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV</code></li><li>No App-V 5,0 SP3, alguns registros foram consolidados e movidos para o seguinte local:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</code><p><p>Para obter uma lista dos logs movidos, consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</li><li>Os pacotes armazenados atualmente em computadores que executam o cliente App-V 5,0 são salvos no seguinte local:<p><p><code>C:\ProgramData\App-V\<<em>package id</em>>\<<em>version id</em>></code></li></ul>

#### Informações de solução de problemas de instalação do cliente
- Consulte o log de erros na pasta **% Temp%** . 
- Para examinar os arquivos de registro, clique em **Iniciar**, digite **% Temp%** e procure o **log de appv_**. 

## Para instalar o cliente do App-V 5,0

1. Copie o arquivo de instalação do cliente do App-V 5,0 para o computador em que ele será instalado.<p><p>Escolha um dos seguintes tipos de cliente:


   |                  Tipo de cliente                  |          Arquivo a ser usado          |
   |-----------------------------------------------|-------------------------------|
   |        Versão padrão do cliente         |   **appv_client_setup.exe**   |
   | Versão dos serviços de área de trabalho remota do cliente | **appv_client_setup_rds.exe** |

   ---

2. Clique duas vezes no arquivo de instalação e clique em **instalar**. Antes da instalação começar, o instalador verifica o computador em busca de [pré-requisitos do App-V 5,0](app-v-50-prerequisites.md)ausentes.

3. Revise e aceite os termos de licença para software, escolha se deseja usar o Microsoft Update e se quer participar do programa de aperfeiçoamento da experiência do usuário da Microsoft e clique em **instalar**.

4. Na página **configuração concluída com êxito** , clique em **fechar**.

   A instalação cria as seguintes entradas para o cliente App-V nos **programas**:

   -   **.exe**

   -   **.msi**

   -   **pacote de idiomas**

   >[!NOTE]
   >Após a instalação, somente o arquivo. exe pode ser desinstalado.


## Para instalar o cliente do App-V 5,0 usando um script

1. Instale todo o software de pré-requisito obrigatório nos computadores de destino. Veja [o que fazer antes de começar](#bkmk-clt-install-prereqs). Se você instalar o cliente usando um arquivo. msi, a instalação falhará se algum pré-requisito estiver ausente.

2. Para usar um script para instalar o cliente App-V 5,0, use os parâmetros a seguir com **appv\_client\_setup.exe**.

   >[!NOTE]
   >O Windows Installer (. msi) do cliente oferece suporte ao mesmo conjunto de opções, exceto para o parâmetro **/log** .

   |                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   |----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |           /INSTALLDIR            |                                                                                                                                                               Especifica o diretório de instalação. Exemplo de uso:<p><p>**/INSTALLDIR = C:\Program Files\AppV cliente**                                                                                                                                                                |
   |            /CEIPOPTIN            |                                                                                                                                                          Habilita a participação no programa de aperfeiçoamento da experiência do usuário. Exemplo de uso:<p><p>**/CEIPOPTIN = [0 \ | 1 \]**                                                                                                                                                           |
   |             /MUOPTIN             |                                                                                                                                                                                 Habilita o Microsoft Update. Exemplo de uso:<p><p>**/MUOPTIN = [0 \ | 1 \]**                                                                                                                                                                                  |
   |     /PACKAGEINSTALLATIONROOT     |                                                                                                                                         Especifica o diretório no qual instalará todos os novos aplicativos e atualizações. Exemplo de uso: <p><p>**/PACKAGEINSTALLATIONROOT = "pacotes C:\App-V"**                                                                                                                                         |
   |        /PACKAGESOURCEROOT        |                                                                                                                                                  Substitui o local de origem para baixar o conteúdo do pacote. Exemplo de uso:<p><p>**/PACKAGESOURCEROOT = ' <http://packageStore> '**                                                                                                                                                  |
   |            /AUTOLOAD             |                                                                                           Especifica como novos pacotes serão carregados pelo App-V 5,0 em um computador específico. As opções a seguir estão habilitadas: [1]; carregar automaticamente todos os pacotes [2]; ou carregar automaticamente nenhum pacote [0]. Exemplo de uso:<p><p>**/AUTOLOAD = [0 \ | 1 \ | 2 \]**                                                                                           |
   |     /SHAREDCONTENTSTOREMODE      |                                                                                                                                           Especifica que o conteúdo do pacote em fluxo não será salvo no disco rígido local. Exemplo de uso: <p><p>**/SHAREDCONTENTSTOREMODE = [0 \ | 1 \]**                                                                                                                                            |
   |          /MIGRATIONMODE          |                                                                                                                     Permite que o cliente do App-V 5,0 modifique os atalhos e FTAs associados aos pacotes criados com uma versão anterior. Exemplo de uso:<p><p>**/MIGRATIONMODE = [0 \ | 1 \]**                                                                                                                     |
   |      /ENABLEPACKAGESCRIPTS       |                                                                                                                                   Habilita os scripts definidos no arquivo de manifesto do pacote ou arquivos de configuração que devem ser executados. Exemplo de uso:<p><p>**/ENABLEPACKAGESCRIPTS = [0 \ | 1 \]**                                                                                                                                   |
   |    /ROAMINGREGISTRYEXCLUSIONS    |                                                                                                                                      Especifica os caminhos do registro que não serão movidos para um perfil de usuário. Exemplo de uso:<p><p>**/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients**                                                                                                                                      |
   |      /ROAMINGFILEEXCLUSIONS      |                                                                                                                                  Especifica os caminhos de arquivo relativos a% USERPROFILE% que não fazem roaming com um perfil de usuário. Exemplo de uso: <p><p>**/ROAMINGFILEEXCLUSIONS ' área de trabalho '; minhas imagens '**                                                                                                                                   |
   |   /S [1-5] PUBLISHINGSERVERNAME    |                                                                                                                                                           Exibe o nome do servidor de publicação. Exemplo de uso:<p><p>**/S2PUBLISHINGSERVERNAME = MyPublishingServer**                                                                                                                                                            |
   |    /S [1-5] PUBLISHINGSERVERURL    |                                                                                                                                                                Exibe a URL do servidor de publicação. Exemplo de uso:<p><p>**/S2PUBLISHINGSERVERURL = \\pubserver**                                                                                                                                                                |
   |   /S [1-5] GLOBALREFRESHENABLED    |                                                                                                                                                                    Habilita uma atualização de publicação global. Exemplo de uso:<p><p>**/S2GLOBALREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                     |
   |   /S [1-5] GLOBALREFRESHONLOGON    |                                                                                                                                                             Inicia uma atualização de publicação global quando um usuário faz logon. Exemplo de uso:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                              |
   |   /S [1-5] GLOBALREFRESHINTERVAL   |                                                                                                                                         Especifica o intervalo de atualização de publicação, em que **0** indica que a atualização não é periódica. Exemplo de uso: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   | /S [1-5] GLOBALREFRESHINTERVALUNIT |                                                                                                                                                            Especifica a unidade de intervalo (horas [0], dias [1]). Exemplo de uso:<p><p>**/S2GLOBALREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                            |
   |    /S [1-5] USERREFRESHENABLED     |                                                                                                                                                                          Permite a atualização da publicação do usuário. Exemplo de uso: **/S2USERREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                          |
   |    /S [1-5] USERREFRESHONLOGON     |                                                                                                                                                              Inicia uma atualização de publicação do usuário quando um usuário faz logon. Exemplo de uso:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                               |
   |    /S [1-5] USERREFRESHINTERVAL    |                                                                                                                                         Especifica o intervalo de atualização de publicação, em que **0** indica que a atualização não é periódica. Exemplo de uso: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   |  /S [1-5] USERREFRESHINTERVALUNIT  |                                                                                                                                                             Especifica a unidade de intervalo (horas [0], dias [1]). Exemplo de uso:<p><p>**/S2USERREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                             |
   |               /Log               |                                                                                                                                                Especifica um local onde as informações do log são salvas. O local padrão é% Temp%. Exemplo de uso:<p><p>**/log C:\logs\log.log**                                                                                                                                                |
   |                /q                |                                                                                                                                                                                                Especifica uma instalação autônoma.                                                                                                                                                                                                |
   |             /REPAIR              |                                                                                                                                                                                               Repara uma instalação anterior do cliente.                                                                                                                                                                                               |
   |            /NORESTART            | Impede que o computador reinicie após a instalação do cliente.<p><p>O parâmetro impede que o computador do usuário final reinicie a reinicialização após a instalação de cada atualização e permite que você agende a reinicialização da sua conveniência. Por exemplo, você pode instalar o App-V 5,0 SPX e, em seguida, instalar o pacote de hotfix Y sem reinicialização após a instalação do Service Pack. Após a instalação, você deve reinicializar antes de começar a usar o App-V. |
   |            /UNINSTALL            |                                                                                                                                                                                                       Desinstala o cliente.                                                                                                                                                                                                        |
   |           /ACCEPTEULA            |                                                                                                                                              Aceita o contrato de licença. Isso é necessário para uma instalação automática. Exemplo de uso:<p><p>**/AcceptEula** ou **/ACCEPTEULA = 1**                                                                                                                                               |
   |             /LAYOUT              |                                                                                                                               Especifica a ação de layout associado. Ele também extrai o Windows Installer (. msi) e arquivos de script para uma pasta sem instalar o App-V 5,0. Nenhum valor é esperado.                                                                                                                                |
   |            /LAYOUTDIR            |                                                                                                                                                 Especifica o diretório de layout. Requer um valor de cadeia de caracteres. Exemplo de uso:<p><p>**/LAYOUTDIR = "cliente de virtualização C:\Application"**                                                                                                                                                  |
   |          /?,/h,/Help           |                                                                                                                                                                                      Solicita ajuda sobre os parâmetros de instalação anteriores.                                                                                                                                                                                      |

   ---

## Para instalar o cliente do App-V 5,0 usando o arquivo do Windows Installer (. msi)

1. Instale os pré-requisitos obrigatórios nos computadores de destino. Veja [o que fazer antes de começar](#bkmk-clt-install-prereqs). Se algum pré-requisito não for atendido, a instalação irá falhar.

2. Certifique-se de que os computadores de destino não tenham reinícios pendentes antes de instalar o cliente usando os arquivos do Windows Installer (. msi) do App-V 5,0. Os arquivos do Windows Installer não sinalizam uma reinicialização pendente.

3. Implante um dos seguintes arquivos do Windows Installer para o computador de destino. O arquivo especificado deve corresponder à configuração do computador de destino.


   |                       Tipo de implantação                        |      Implantar este arquivo       |
   |-----------------------------------------------------------------|-----------------------------|
   | O computador está executando um sistema operacional Microsoft Windows de 32 bits |   appv_client_MSI_x86.msi   |
   | O computador está executando um sistema operacional Microsoft Windows de 64 bits |   appv_client_MSI_x64.msi   |
   | Você está implantando o cliente dos serviços de área de trabalho remota do App-V 5,0  | appv_client_rds_MSI_x64.msi |

   ---

4. Usando as informações da tabela a seguir, selecione o pacote de idiomas apropriado para instalar, com base no idioma **desejado para o** computador de destino. O **xxxx** na tabela refere-se à localidade de destino do pacote de idiomas.

   **O que saber antes de começar:** 

   -  Os pacotes de idiomas são comuns ao cliente padrão do App-V 5,0 e à versão dos serviços de área de trabalho remota do App-V 5,0 Client.

   -  Se você instalar o cliente do App-V 5,0 usando o **. exe**, o instalador implantará apenas o pacote de idiomas que corresponde ao sistema operacional em execução no computador de destino.

   -  Para implantar pacotes de idiomas adicionais em um computador de destino, use o procedimento **para instalar o cliente do App-V 5,0 usando o arquivo do Windows Installer (. msi)**.

   |                       Tipo de implantação                        |       Implantar este arquivo       |
   |-----------------------------------------------------------------|------------------------------|
   | O computador está executando um sistema operacional Microsoft Windows de 32 bits | appv_client_LP_xxxx_ x86.msi |
   | O computador está executando um sistema operacional Microsoft Windows de 64 bits | appv_client_LP_xxxx_ x64.msi |

   ---

   **Tem uma sugestão para o App-V**? Adicionar ou votar em [sugestões](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). <p><p>**Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Implantação do App-V 5.0](deploying-app-v-50.md)

[Sobre as configurações do cliente](about-client-configuration-settings.md)

[Como desinstalar o cliente do App-V 5.0](how-to-uninstall-the-app-v-50-client.md)
