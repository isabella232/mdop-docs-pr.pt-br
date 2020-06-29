---
title: Notas de versão do App-V 4.5 SP2
description: Notas de versão do App-V 4.5 SP2
author: dansimp
ms.assetid: 1b3a8a83-4523-4634-9f75-29bc22ca5815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 35cff3b2a2c110a4d8beba883a4cf9332381ea60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797608"
---
# Notas de versão do App-V 4.5 SP2


Para pesquisar essas notas de versão, pressione CTRL + F.

**Importante**  Leia estas notas de versão cuidadosamente antes de instalar o sistema de gerenciamento do Microsoft Application Virtualization. Estas notas da versão contêm informações que você precisa para instalar o sistema de gerenciamento do Application Virtualization com êxito. Estas notas da versão contêm informações que não estão disponíveis na documentação do produto. Se houver discrepância entre essas notas de versão e outras documentações do sistema de gerenciamento do aplicativo Virtualization, a alteração mais recente deve ser considerada autorizada.

 

Para obter informações atualizadas sobre problemas conhecidos, acesse a biblioteca do Microsoft TechNet nas [notas de versão do App-V 4,5 SP2](https://go.microsoft.com/fwlink/?LinkId=184640) ( https://go.microsoft.com/fwlink/?LinkId=184640) .

## Sobre o Microsoft Application Virtualization 4,5 Service Pack 2


Estas notas de versão foram atualizadas para refletir as alterações introduzidas com o Microsoft Application Virtualization (App-V) 4.5 Service Pack2 (SP2). Este Service Pack contém as seguintes alterações:

-   Suporte para o Office 2010: o App-V 4.5 SP2 agora oferece suporte à virtualização do Microsoft Office 2010. Para obter orientação prescritiva para o Microsoft Office 2010 com o App-V 4,5 SP2, consulte [orientação prescritiva para sequenciamento do office 2010 no Microsoft App-v 4,6](https://go.microsoft.com/fwlink/?LinkId=191539) ( https://go.microsoft.com/fwlink/?LinkId=191539) .

-   Suporte para espelhamento de banco de dados: o App-V 4.5 SP2 agora oferece suporte ao espelhamento de banco de dados do Microsoft SQL Server. Para obter mais informações sobre como configurar o espelhamento de banco de dados em seu ambiente App-V, consulte [como configurar o suporte ao espelhamento do Microsoft SQL Server para app-v](https://go.microsoft.com/fwlink/?LinkId=190880) ( https://go.microsoft.com/fwlink/?LinkId=190880) .

-   Feedback do cliente e pacote cumulativo de hotfix: App-V 4.5 o SP2 também inclui um pacote cumulativo de correções para solucionar problemas encontrados após a versão do App-V 4.5 SP1. As atualizações abordam uma combinação de problemas conhecidos e comentários dos clientes de equipes internas, parceiros e clientes da Microsoft que usam o App-V 4.5. Para obter uma lista completa das atualizações, consulte o artigo 980847 na base de dados de conhecimento Microsoft (KB) na [Descrição do Microsoft Application Virtualization 4,5 Service Pack 2](https://go.microsoft.com/fwlink/?LinkId=191540) ( https://go.microsoft.com/fwlink/?LinkId=191540) .

## Sobre a documentação do produto


A documentação abrangente do Application Virtualization (App-V) está disponível no Microsoft TechNet na [biblioteca do TechCenter do Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) . A documentação do TechNet inclui a ajuda online para o Application Virtualization Sequencer, os clientes do Application Virtualization e o servidor do Application Virtualization. Ele também inclui o guia de planejamento e implantação do Application Virtualization e o guia de operações de virtualização de aplicativo.

## Proteger contra vulnerabilidades e vírus de segurança


Para ajudar a proteger contra vulnerabilidades e vírus de segurança, recomendamos que você instale as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado. Para obter mais informações, consulte [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Fornecer comentários


Você pode enviar comentários, fazer uma sugestão ou relatar um problema com o sistema de gerenciamento do Microsoft Application Virtualization (App-V) por meio do fórum da Comunidade no fórum da documentação do Application Virtualization TechCenter [App-V](https://go.microsoft.com/fwlink/?LinkId=122917) https://go.microsoft.com/fwlink/?LinkId=122917) .

Você também pode enviar seus comentários sobre a documentação diretamente para a equipe de documentação do App-V em <appvdocs@microsoft.com> .

## Problemas conhecidos do Application Virtualization 4.5 SP2


Esta seção fornece as informações mais atualizadas sobre problemas com o Microsoft Application Virtualization (App-V) 4.5 SP2. Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto. Sempre que possível, esses problemas serão abordados em lançamentos posteriores do software.

### Orientação para instalar o console de gerenciamento do servidor

Se você precisar instalar o software de gerenciamento em sistemas diferentes do servidor principal de publicação e streaming do Application Virtualization, a instalação do servidor oferece suporte à instalação do console de gerenciamento do Application Virtualization e do Web Service de gerenciamento do Application Virtualization em servidores separados do servidor de gerenciamento do App-V primário. Para distribuir os componentes de gerenciamento em vários servidores, a delegação Kerberos deve estar habilitada no servidor em que o serviço Web do Application Virtualization está instalado. Para obter informações sobre como habilitar esse suporte, consulte [como configurar o servidor para ser confiável para delegação](https://go.microsoft.com/fwlink/?LinkId=166682) ( https://go.microsoft.com/fwlink/?LinkId=166682) .

### Orientação para instalar ou atualizar clientes para o App-V 4.5 SP2 usando o Setup.msi

Ao instalar ou atualizar seus clientes do App-V para o App-V 4,5 SP2 usando Setup.msi, os pré-requisitos não são instalados automaticamente.

O WORKAROUNDYou deve instalar manualmente os pré-requisitos antes de instalar ou atualizar os clientes do App-V para o App-V 4.5 SP2. Para obter procedimentos detalhados sobre como instalar os pré-requisitos e o cliente App-V, consulte [como instalar o cliente usando a linha de comando](https://go.microsoft.com/fwlink/?LinkId=144106) ( https://go.microsoft.com/fwlink/?LinkId=144106) .

Quando isso tiver sido concluído, instale os clientes do App-V 4,5 SP2 usando Setup.msi com credenciais administrativas. Esse arquivo está disponível na mídia de lançamento do App-V 4,5 SP2 na pasta Installers\\Client

Ao instalar o relatório de erros do aplicativo Microsoft, use o seguinte comando se você estiver instalando ou atualizando para o cliente da área de trabalho do App-V 4,5 SP2:

**msiexec/i dw20shared.msi APPGUID = {C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D} AllUsers = 1 reboot = supressão REINSTALL = ALL REINSTALLMODE = vomus**

Como alternativa, se você estiver instalando ou atualizando para o cliente do App-V 4,5 SP2 para serviços de área de trabalho remota (antes serviços de terminal), use o seguinte comando:

**msiexec/i dw20shared.msi APPGUID = {ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5} AllUsers = 1 reboot = supressão REINSTALL = ALL REINSTALLMODE = vomus**

**Observação**  
-   O parâmetro APPGUID referencia o código do produto dos clientes App-V que você instala ou atualiza. O código do produto é exclusivo para cada Setup.msi. Você pode usar o editor de banco de dados Orca ou uma ferramenta semelhante para examinar os arquivos do Windows Installer e determinar o código do produto. Esta etapa é necessária para todas as instalações ou atualizações para o App-V 4,5 SP2.

-   Esta etapa não será necessária se você estiver atualizando e tiver instalado Dw20shared.msi anteriormente.

 

### Melhorar o desempenho ao sequenciar o .NET Framework

Ao sequenciar o Microsoft .NET Framework, você pode enfrentar um desempenho de sistema reduzido porque o serviço NGEN do .NET Framework tenta pré-compilar assemblies como uma tarefa em segundo plano.

WORKAROUNDWhen sequenciando o .NET Framework, desabilite o .NET Framework NGEN Service (Mscorsvw.exe) após concluir a fase de monitoramento. Você deve usar a guia de **Serviços virtuais** no sequenciador do App-V e alterar o tipo de inicialização para **desabilitado**.

### Ao desinstalar o cliente do Microsoft Application Virtualization, as configurações do usuário associadas ao usuário que está realizando a desinstalação serão excluídas

Quando você desinstalar o cliente App-V, o Windows Installer removerá as configurações do aplicativo Virtualization do perfil do usuário atual. Se o seu computador usa perfis de roaming, não use sua conta de rede pessoal para desinstalar o cliente porque ele removerá as configurações de seus aplicativos virtuais em todos os seus computadores.

WORKAROUNDYou deve desinstalar o cliente App-V com uma conta administrativa que não é usada para executar aplicativos virtuais.

### As edições feitas nas guias sistema de arquivos virtual e registro virtual devem ser salvas durante a execução do assistente de sequenciamento

Se você abrir um pacote para executar uma atualização, ou se você já tiver executado o assistente de sequenciamento com um novo pacote e fazer alterações no pacote nas guias sistema de arquivos virtual ou registro virtual, essas alterações não serão salvas automaticamente.

WORKAROUNDSave as alterações antes de executar o assistente novamente para garantir que elas sejam refletidas dentro do ambiente virtual do assistente.

### O sequenciador de linha de comando deve ser executado em um prompt de comando elevado

Quando você usa o sequenciador de linha de comando, ele não solicita elevação.

WORKAROUNDRun o sequenciador de linha de comando usando um prompt de comando elevado.

### Nomes de variáveis de caminho curto nos arquivos OSD podem causar erros

Se você receber o erro 450478-1F702339-0000010B "o nome do diretório é inválido" ao iniciar um aplicativo virtual no cliente, é possível que a variável no OSD esteja definida incorretamente. Isso pode acontecer se o instalador do aplicativo definir um nome de caminho curto durante o sequenciamento.

WORKAROUNDRemove o til à direita de qualquer variável CSIDl que exista no arquivo OSD.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Sintaxe correta para o parâmetro DECODEPATH para o sequenciador de linha de comando

No sequenciador de linha de comando, ao abrir um pacote para atualização e decodificá-lo para a raiz da unidade Q, a sintaxe do parâmetro *DECODEPATH* não deve incluir uma barra à direita.

WORKAROUNDYou pode usar **Q:** em vez de **Q:\\** (omitindo o caractere "\ \" à direita).

### <a href="" id="when-upgrading-app-v-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Quando pacotes upgradingAPP-V 4,2, você encontra problemas causados por arquivos do Windows Installer no sistema de arquivos virtual

Durante a atualização de um pacote do APP-V 4.2, você pode enfrentar problemas relacionados a uma incompatibilidade de arquivos de sistema do Windows Installer que foram incluídos por padrão no APP-V 4.2 e nas bibliotecas do Windows Installer instaladas localmente na sua estação de trabalho de sequenciamento. Os arquivos a seguir estão localizados em CSIDl \ _SYSTEM \ \:

Cabinet.dll

Msi.dll

Msiexec.exe

Msihnd.dll

Msimsg.dlll

WORKAROUNDDelete todos os arquivos anteriores do pacote. Exclua os mapeamentos na guia **VFS** e os arquivos reais na pasta CSIDL \ _SYSTEM em seu caminho de decodificação.

### <a href="" id="on-windows-xp--by-default--client-installation-logging-is-not-enabled-"></a>No WindowsXP, por padrão, o log de instalação do cliente não está habilitado

Ao instalar o cliente, para garantir que qualquer erro de instalação seja capturado para solução de problemas, você deve habilitar o log usando a linha de comando.

WORKAROUNDAdd o parâmetro */l\ * VX! log.txt* para a linha de comando, conforme mostrado no exemplo a seguir:

**setup.exe/s/v "/qn/l\ * VX! log.txt "**

**msiexec.exe/i setup.msi/qn/l\ * VX! log.txt**

Você também pode definir a chave do registro como o seguinte valor:

**\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "logging" = "voicewarmupx!"**

### Para que a autenticação Kerberos funcione, os SPNs (nomes principais de serviço) devem ser registrados para o IIS

Ao usar os serviços de informações da Internet (IIS) 6.0 orIIS 7.0 para a recuperação de arquivos do ícone ou do OSD e o streaming de pacotes, para habilitar a autenticação Kerberos, os SPNs devem ser registrados da seguinte maneira:

-   No servidor IIS, execute os seguintes comandos usando a ferramenta kit de recursos do SETSPN.EXE. O nome de domínio totalmente qualificado do servidor (FQDN) deve ser usado.

    **SetSPN-r SOFTGRID/ &lt; servidor FQDN&gt;**

    **SetSPN-r HTTP/ &lt; servidor FQDN&gt;**

Para obter mais informações, consulte [autenticação integrada do Windows (IIS 6,0)](https://go.microsoft.com/fwlink/?LinkId=131407) ( https://go.microsoft.com/fwlink/?LinkId=131407) .

### Alterações de compatibilidade do .NET

O Update1 cumulativo do Microsoft Application Virtualization (App-V) cumulativo ou posterior dá suporte ao sequenciamento do .NET Framework no WindowsXP SP2 ou posterior. As rotinas de sequenciamento para aplicativos .NET que foram escritas para o SoftGrid 4.2 podem precisar ser atualizadas quando usadas com o sequenciador do App-V 4,5. Para obter detalhes e soluções alternativas, consulte o artigo do TechCenter do Application Virtualization em [suporte para .net no Microsoft Application virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=123412) ( https://go.microsoft.com/fwlink/?LinkId=123412) .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Após a atualização do cliente do App-V 4.2, alguns aplicativos não são mostrados

Verifique o seguinte erro no log: "o cliente do Application Virtualization não pôde analisar o arquivo OSD". O cliente App-V 4,5 filtra os aplicativos que têm um arquivo OSD que contém uma marca de sistema operacional vazia ( &lt; &gt; &lt; /os &gt; ).

WORKAROUNDDelete a marca de sistema operacional vazia do arquivo OSD.

### O servidor App-V requer isenções no firewall para certos processos

Para que o servidor transmita os aplicativos corretamente, os processos centrais do servidor, incluindo o Dispatcher, exigem acesso por meio do firewall.

Isenções de contorno no firewall do servidor para os seguintes processos: Sghwsvr.exe e Sghwdsptr.exe. Isso se aplica ao servidor de gerenciamento do App-V e ao App-V Streaming Server.

### Quando o instalador do servidor é executado no modo silencioso, ele não verifica corretamente se o MSXML6

O servidor de gerenciamento do App-V depende do MSXML6. No entanto, se você executar o instalador no modo silencioso — por exemplo, usando o comando **msiexec-i setup.msi/qn** em um sistema em que o MSXML6 ainda não está instalado, o instalador não detecta a dependência ausente e instala assim mesmo. Portanto, quando os clientes tentam atualizar as informações de publicação do servidor de gerenciamento do App-V, eles receberão erros.

WORKAROUNDVerify que o MSXML6 está instalado no sistema antes de tentar uma instalação silenciosa do servidor de gerenciamento do App-V.

### Código de erro 000C800 ao tentar se conectar ao console de gerenciamento do Application Virtualization

Um administrador de virtualização de aplicativos que não é um administrador local no servidor de serviço Web de gerenciamento do App-V recebe um erro (código de erro: 000C800) ao tentar se conectar ao console de gerenciamento do App-V, e a entrada SftMMC. log indica que o acesso a SftMgmt. udl foi negado. Para conectar-se com êxito ao console de gerenciamento do App-V, um administrador que não tem direitos de administrador local no servidor de serviço Web de gerenciamento do App-V deve ter pelo menos permissões de leitura e execução para o arquivo SftMgmt. udl.

Os administradores de virtualização de aplicativos devem ter permissões de leitura e execução para o arquivo SftMgmt. UDL na pasta%systemdrive%\\Program Files\\Microsoft System Center App Virt Management Server\\App Service Management Service.

### Parâmetros de linha de comando do instalador do cliente são ignorados quando usados em conjunto com KEEPCURRENTSETTINGS = 1

Quando usado em conjunto com KEEPCURRENTSETTINGS = 1, os seguintes parâmetros de linha de comando do instalador do cliente são ignorados: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA e REQUIRESECURECONNECTION.

WORKAROUNDIf você tiver configurações que deseja manter, use KEEPCURRENTSETTINGS = 1 e, em seguida, defina os outros parâmetros após a implantação. O modelo App-V ADM pode ser usado para definir as seguintes configurações de cliente: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES e ALLOWINDEPENDENTFILESTREAMING. Você pode baixar o modelo ADM a partir do centro de DownLoad da Microsoft no [modelo administrativo do Microsoft Application Virtualization (modelo ADM)](https://go.microsoft.com/fwlink/?LinkId=121835) ( https://go.microsoft.com/fwlink/?LinkId=121835) .

### Informações de direitos autorais da versão

Este documento é fornecido "na condição em que se encontra". As informações e visualizações apresentadas neste documento, incluindo URL e outras referências a sites, estão sujeitas a alterações sem prévio aviso. Você assume o risco de usá-lo.

Alguns exemplos descritos aqui são fornecidos apenas para ilustração e são fictícios.Nenhuma associação ou conexão real é intencional ou deve ser inferida.

Este documento não fornece direitos legais e nenhuma propriedade intelectual sobre qualquer produto da Microsoft. Você pode copiar e usar este documento para fins de referência interna. Você pode modificar esse documento para suas finalidades de referência internas.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer e Windows Vista são marcas comerciais do grupo de empresas da Microsoft.

Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.

 

 





