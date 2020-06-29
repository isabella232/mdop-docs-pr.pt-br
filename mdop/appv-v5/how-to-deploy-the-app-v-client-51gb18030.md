---
title: Como implantar o cliente do App-V
description: Como implantar o cliente do App-V
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796421"
---
# Como implantar o cliente do App-V


Use o procedimento a seguir para instalar o cliente do Microsoft Application Virtualization (App-V) 5,1 e o cliente de serviços de área de trabalho remota. Você deve instalar a versão do cliente que corresponde ao sistema operacional do computador de destino.

<a href="" id="bkmk-clt-install-prereqs"></a>**O que fazer antes de começar**

1. Revise e instale os pré-requisitos do software:

   Instale o software obrigatório que corresponde à versão do App-V que você está instalando:

   -   [Sobre o App-V 5.1](about-app-v-51.md)

   -   [Pré-requisitos do App-V 5.1](app-v-51-prerequisites.md)

2. Revise os cenários de coexistência e sem suporte do cliente, conforme aplicável à sua instalação:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Implantando clientes App-V coexistentes</p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)">Planejamento para a implantação do sequenciador e do cliente do App-V 5.1</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Cenários de instalação sem suporte ou limitados</p></td>
   <td align="left"><p>Consulte a seção cliente nas <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurações com suporte do App-V 5,1</a></p></td>
   </tr>
   </tbody>
   </table>



3. Examine os locais do registro do cliente, log e informações de solução de problemas:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Informações do registro do cliente</p></td>
<td align="left"><ul>
<li><p>Por padrão, depois de instalar o cliente App-V 5,1, as informações do cliente são armazenadas no registro na seguinte chave do registro:</p>
<p><strong>HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENTE</strong></p></li>
<li><p>Quando você implanta um pacote virtualizado em um computador que está executando o cliente App-V, os dados do pacote associado são armazenados no seguinte local:</p>
<p><strong>C: \ ProgramData \ App-V</strong></p>
<p>No entanto, você pode reconfigurar esse local com a seguinte chave do registro:</p>
<p><strong>HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENTE \ STREAMING \ PACKAGEINSTALLATIONROOT</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Arquivos de log do cliente</p></td>
<td align="left"><ul>
<li><p>Para informações do arquivo de log associadas ao cliente App-V 5,1, pesquise no seguinte log:</p>
<p><strong>Logs de eventos/aplicativos e serviços Logs/Microsoft/AppV</strong></p></li>
<li><p>No App-V 5,0 SP3, alguns registros foram consolidados e movidos para o seguinte local:</p>
<p><strong>Logs de eventos/aplicativos e serviços Logs/Microsoft/AppV/ServiceLog</strong></p>
<p>Para obter uma lista dos logs movidos, consulte <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> sobre o App-V 5,0 SP3 </a> .</p></li>
<li><p>Os pacotes armazenados atualmente em computadores que executam o cliente App-V 5,1 são salvos no seguinte local:</p>
<p><strong>C:\ProgramData\App-V &amp; lt; ID do pacote &gt; &amp; lt; ID da versão&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Informações de solução de problemas de instalação do cliente</p></td>
<td align="left"><p>Consulte o log de erros na <strong> pasta% temp% </strong> . Para examinar os arquivos de registro, clique em <strong> Iniciar </strong> , digite <strong> % temp% </strong> e procure o <strong> log de appv_ </strong> .</p></td>
</tr>
</tbody>
</table>



**Para instalar o cliente do App-V 5,1**

1.  Copie o arquivo de instalação do cliente do App-V 5,1 para o computador em que ele será instalado. Escolha um dos seguintes tipos de cliente:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo de cliente</th>
    <th align="left">Arquivo a ser usado</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Versão padrão do cliente</p></td>
    <td align="left"><p><strong>appv_client_setup.exe</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Versão dos serviços de área de trabalho remota do cliente</p></td>
    <td align="left"><p><strong>appv_client_setup_rds.exe</strong></p></td>
    </tr>
    </tbody>
    </table>



2.  Clique duas vezes no arquivo de instalação e clique em **instalar**. Antes da instalação começar, o instalador verifica o computador em busca de [pré-requisitos do App-V 5,1](app-v-51-prerequisites.md)ausentes.

3.  Revise e aceite os termos de licença para software, escolha se deseja usar o Microsoft Update e se quer participar do programa de aperfeiçoamento da experiência do usuário da Microsoft e clique em **instalar**.

4.  Na página **configuração concluída com êxito** , clique em **fechar**.

    A instalação cria as seguintes entradas para o cliente App-V nos **programas**:

    -   **.exe**

    -   **.msi**

    -   **pacote de idiomas**

        **Observação**  
        Após a instalação, somente o arquivo. exe pode ser desinstalado.



**Para instalar o cliente do App-V 5,1 usando um script**

1. Instale todo o software de pré-requisito obrigatório nos computadores de destino. Veja [o que fazer antes de começar](#bkmk-clt-install-prereqs). Se você instalar o cliente usando um arquivo. msi, a instalação falhará se algum pré-requisito estiver ausente.

2. Para usar um script para instalar o cliente App-V 5,1, use os parâmetros a seguir com **appv\_client\_setup.exe**.

   **Observação**  
   O Windows Installer (. msi) do cliente oferece suporte ao mesmo conjunto de opções, exceto para o parâmetro **/log** .

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>/INSTALLDIR</p></td>
   <td align="left"><p>Especifica o diretório de instalação. Exemplo de uso: <strong> /installdir = C:\Program Files\AppV Client</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/CEIPOPTIN</p></td>
   <td align="left"><p>Habilita a participação no programa de aperfeiçoamento da experiência do usuário. Exemplo de uso: <strong> /CEIPOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/MUOPTIN</p></td>
   <td align="left"><p>Habilita o Microsoft Update. Exemplo de uso: <strong> /MUOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/PACKAGEINSTALLATIONROOT</p></td>
   <td align="left"><p>Especifica o diretório no qual instalará todos os novos aplicativos e atualizações. Exemplo de uso: <strong> /PACKAGEINSTALLATIONROOT = pacotes C:\App-V de&#39;&#39;</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/PACKAGESOURCEROOT</p></td>
   <td align="left"><p>Substitui o local de origem para baixar o conteúdo do pacote. Exemplo de uso: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/AUTOLOAD</p></td>
   <td align="left"><p>Especifica como novos pacotes serão carregados pelo App-V 5,1 em um computador específico. As opções a seguir estão habilitadas: [1]; carregar automaticamente todos os pacotes [2]; ou carregar automaticamente nenhum pacote [0]. <strong> Exemplo de uso:/AUTOLOAD = [0 | 1 | 2]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/SHAREDCONTENTSTOREMODE</p></td>
   <td align="left"><p>Especifica que o conteúdo do pacote em fluxo não será salvo no disco rígido local. Exemplo de uso: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/MIGRATIONMODE</p></td>
   <td align="left"><p>Permite que o cliente do App-V 5,1 modifique os atalhos e FTAs associados aos pacotes criados com uma versão anterior. Exemplo de uso: <strong> /MIGRATIONMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ENABLEPACKAGESCRIPTS</p></td>
   <td align="left"><p>Habilita os scripts definidos no arquivo de manifesto do pacote ou arquivos de configuração que devem ser executados. Exemplo de uso: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/ROAMINGREGISTRYEXCLUSIONS</p></td>
   <td align="left"><p>Especifica os caminhos do registro que não serão movidos para um perfil de usuário. Exemplo de uso: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ROAMINGFILEEXCLUSIONS</p></td>
   <td align="left"><p>Especifica os caminhos de arquivo relativos a% USERPROFILE% que não fazem roaming com um perfil de usuário&#39;s. Exemplo de uso: <strong> /ROAMINGFILEEXCLUSIONS área de trabalho do &#39;; minhas imagens&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERNAME</p></td>
   <td align="left"><p>Exibe o nome do servidor de publicação. Exemplo de uso: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERURL</p></td>
   <td align="left"><p>Exibe a URL do servidor de publicação. Exemplo de uso: <strong> /S2PUBLISHINGSERVERURL = \pubserver</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHENABLED-</p></td>
   <td align="left"><p>Habilita uma atualização de publicação global. Exemplo de uso: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHONLOGON</p></td>
   <td align="left"><p>Inicia uma atualização de publicação global quando um usuário faz logon. Exemplo de uso: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVAL-</p></td>
   <td align="left"><p>Especifica o intervalo de atualização de publicação, em que <strong> 0 indica que a </strong> atualização não é periódica. Exemplo de uso: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Especifica a unidade de intervalo (horas [0], dias [1]). Exemplo de uso: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHENABLED</p></td>
   <td align="left"><p>Permite a atualização da publicação do usuário. Exemplo de uso: <strong> /S2USERREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHONLOGON</p></td>
   <td align="left"><p>Inicia uma atualização de publicação do usuário quando um usuário faz logon. Exemplo de uso: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVAL-</p></td>
   <td align="left"><p>Especifica o intervalo de atualização de publicação, em que <strong> 0 indica que a </strong> atualização não é periódica. Exemplo de uso: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Especifica a unidade de intervalo (horas [0], dias [1]). Exemplo de uso: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/Log</p></td>
   <td align="left"><p>Especifica um local onde as informações do log são salvas. O local padrão é% Temp%. Exemplo de uso: <strong> /log C:\logs\log.log</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/q</p></td>
   <td align="left"><p>Especifica uma instalação autônoma.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/REPAIR</p></td>
   <td align="left"><p>Repara uma instalação anterior do cliente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/NORESTART</p></td>
   <td align="left"><p>Impede que o computador reinicie após a instalação do cliente.</p>
   <p>O parâmetro impede que o computador do usuário final reinicie a reinicialização após a instalação de cada atualização e permite que você agende a reinicialização da sua conveniência. Por exemplo, você pode instalar o App-V 5,1 e, em seguida, instalar o pacote de hotfix Y sem reinicialização após a instalação do Service Pack. Após a instalação, você deve reinicializar antes de começar a usar o App-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/UNINSTALL</p></td>
   <td align="left"><p>Desinstala o cliente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ACCEPTEULA</p></td>
   <td align="left"><p>Aceita o contrato de licença. Isso é necessário para uma instalação automática. Exemplo de uso: <strong> /AcceptEula </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/LAYOUT</p></td>
   <td align="left"><p>Especifica a ação de layout associado. Ele também extrai o Windows Installer (. msi) e arquivos de script para uma pasta sem instalar o App-V 5,1. Nenhum valor é esperado.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/LAYOUTDIR</p></td>
   <td align="left"><p>Especifica o diretório de layout. Requer um valor de cadeia de caracteres. Exemplo de uso: <strong> /LAYOUTDIR = "cliente de virtualização C:\Application" </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/?,/h,/Help</p></td>
   <td align="left"><p>Solicita ajuda sobre os parâmetros de instalação anteriores.</p></td>
   </tr>
   </tbody>
   </table>



**Para instalar o cliente do App-V 5,1 usando o arquivo do Windows Installer (. msi)**

1.  Instale os pré-requisitos obrigatórios nos computadores de destino. Veja [o que fazer antes de começar](#bkmk-clt-install-prereqs). Se algum pré-requisito não for atendido, a instalação irá falhar.

2.  Certifique-se de que os computadores de destino não tenham reinícios pendentes antes de instalar o cliente usando os arquivos do Windows Installer (. msi) do App-V 5,1. Os arquivos do Windows Installer não sinalizam uma reinicialização pendente.

3.  Implante um dos seguintes arquivos do Windows Installer para o computador de destino. O arquivo especificado deve corresponder à configuração do computador de destino.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo de implantação</th>
    <th align="left">Implantar este arquivo</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>O computador está executando um sistema operacional Microsoft Windows de 32 bits</p></td>
    <td align="left"><p>appv_client_MSI_x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>O computador está executando um sistema operacional Microsoft Windows de 64 bits</p></td>
    <td align="left"><p>appv_client_MSI_x64.msi</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Você está implantando o cliente dos serviços de área de trabalho remota do App-V 5,1</p></td>
    <td align="left"><p>appv_client_rds_MSI_x64.msi</p></td>
    </tr>
    </tbody>
    </table>



4.  Usando as informações da tabela a seguir, selecione o pacote de idiomas apropriado para instalar, com base no idioma **desejado para o** computador de destino. O **xxxx** na tabela refere-se à localidade de destino do pacote de idiomas.

    **O que saber antes de começar:**

    -   Os pacotes de idiomas são comuns ao cliente padrão do App-V 5,1 e à versão dos serviços de área de trabalho remota do App-V 5,1 Client.

    -   Se você instalar o cliente do App-V 5,1 usando o **. exe**, o instalador implantará apenas o pacote de idiomas que corresponde ao sistema operacional em execução no computador de destino.

    -   Para implantar pacotes de idiomas adicionais em um computador de destino, use o procedimento **para instalar o cliente do App-V 5,1 usando o arquivo do Windows Installer (. msi)**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo de implantação</th>
    <th align="left">Implantar este arquivo</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>O computador está executando um sistema operacional Microsoft Windows de 32 bits</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>O computador está executando um sistema operacional Microsoft Windows de 64 bits</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x64.msi</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Tópicos relacionados


[Implantação do App-V 5.1](deploying-app-v-51.md)

[Sobre as configurações do cliente](about-client-configuration-settings51.md)

[Como desinstalar o cliente do App-V 5.1](how-to-uninstall-the-app-v-51-client.md)









