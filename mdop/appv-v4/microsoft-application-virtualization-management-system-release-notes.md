---
title: Notas da versão do sistema de gerenciamento do Microsoft Application Virtualization
description: Notas da versão do sistema de gerenciamento do Microsoft Application Virtualization
author: dansimp
ms.assetid: e1a4d5ee-53c7-4b48-814c-a34ce0e698dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c34abab9a49bd69f760a9b531d0950cc581253c1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796870"
---
# Notas da versão do sistema de gerenciamento do Microsoft Application Virtualization


Para pesquisar essas notas de versão, pressione CTRL + F.

**Importante**  Leia estas notas de versão cuidadosamente antes de instalar o sistema de gerenciamento do Application Virtualization. Estas notas da versão contêm informações que você precisa para instalar o sistema de gerenciamento do Application Virtualization com êxito. Este documento contém informações que não estão disponíveis na documentação do produto. Se houver discrepância entre essas notas de versão e outras documentações do sistema de gerenciamento do aplicativo Virtualization, a alteração mais recente deve ser considerada autorizada. Estas notas de versão substituem o conteúdo incluído neste produto.

 

Para obter informações atualizadas sobre problemas conhecidos, acesse a biblioteca do Microsoft TechNet em <https://go.microsoft.com/fwlink/?LinkId=122918> .

## Sobre a atualização cumulativa 1 do Microsoft Application Virtualization 4,5


Estas notas de versão foram atualizadas para refletir as alterações introduzidas com o Microsoft Application Virtualization 4.5 cumulativo Update1 (App-V 4.5 CU1), que fornece as atualizações mais recentes para o Application Virtualization (App-V) 4.5. Esta atualização cumulativa contém as seguintes alterações:

-   Suporte para o Windows7 beta e Windows Server2008R2 beta: o App-V 4.5 CU1 aborda problemas de compatibilidade com o Windows7 beta e o Windows Server2008R2 beta. O suporte será fornecido para problemas de bloqueio que impedem o App-V 4.5 CU1 em execução em um ambiente de teste nas versões anteriores ao RTM do Windows7. Isso ajudará a garantir que seus aplicativos virtuais possam ser executados com êxito em um ambiente de teste em que a compatibilidade entre o cliente do App-V 4.5 e o Windows7 beta é necessária.

    **Importante**  Não há suporte para a execução do App-V 4.5 CU1 em qualquer versão do Windows7 ou Windows Server2008R2 em um ambiente operacional dinâmico.

     

-   Suporte aprimorado para a sequenciamento o .NET Framework: App-V 4.5 CU1 aborda problemas anteriores com o sequenciamento do .NET Framework 3.5 e versões anteriores no WindowsXP (SP2 ou posterior). Para obter mais informações sobre os novos recursos, consulte o artigo do TechNet em <https://go.microsoft.com/fwlink/?LinkId=123412> .

-   Feedback do cliente e pacote cumulativo de hotfix: App-V 4.5 o CU1 também inclui um acúmulo de correções para solucionar problemas encontrados desde a versão RTM do App-V 4.5. Isso inclui uma combinação de problemas conhecidos e comentários dos clientes de nossas equipes internas, parceiros e clientes que usam o App-V 4.5. Para obter uma lista completa das atualizações incluídas, consulte o artigo da base de conhecimento em <https://go.microsoft.com/fwlink/?LinkId=141258> .

## Sobre a documentação do produto


A documentação abrangente da virtualização de aplicativos (App-V) está disponível no Microsoft TechNet no TechCenter Application Virtualization (App-V) em <https://go.microsoft.com/fwlink/?LinkId=122939> . A documentação do TechNet inclui a ajuda online para o Application Virtualization Sequencer, o cliente Application Virtualization e o servidor Application Virtualization. Ele também inclui o guia de planejamento e implantação do Application Virtualization e o guia de operações de virtualização de aplicativo.

## Proteger contra vulnerabilidades e vírus de segurança


Para ajudar a proteger contra vulnerabilidades e vírus de segurança, é importante instalar as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado. Para obter mais informações, consulte o site de segurança da Microsoft em <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Como fornecer comentários


Você pode enviar comentários, fazer uma sugestão ou relatar um problema com o sistema de gerenciamento do Microsoft Application Virtualization (App-V) por meio de um fórum da Comunidade no Microsoft Application Virtualization TechCenter ( <https://go.microsoft.com/fwlink/?LinkId=122917> ).

Você também pode fornecer seus comentários sobre a documentação diretamente para a equipe de documentação do App-V. Envie seus comentários sobre a documentação para appvdocs@microsoft.com.

## Problemas conhecidos com o Application Virtualization 4.5 CU1


Esta seção fornece as informações mais atualizadas sobre problemas com o Microsoft Application Virtualization (App-V) 4.5 CU1. Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto. Sempre que possível, esses problemas serão resolvidos em versões posteriores.

### Orientação para instalar ou atualizar clientes para o App-V 4.5 CU1 usando o setup.msi

Ao instalar ou atualizar seus clientes do App-V para o App-V 4.5 CU1 usando setup.msi, os pré-requisitos não são instalados automaticamente.

O WORKAROUNDYou deve instalar manualmente os pré-requisitos antes de instalar ou atualizar o cliente App-V para 4.5 CU1. Para obter procedimentos detalhados de instalação dos pré-requisitos e do cliente App-V, consulte <https://go.microsoft.com/fwlink/?LinkId=144106> .

Quando isso tiver sido concluído, instale o aplicativo App-V 4.5 CU1 o cliente usando setup.msi com privilégios elevados. Esse arquivo está disponível na mídia de lançamento do App-V 4.5 CU1 na pasta Installers\\Client.

Ao instalar o relatório de erros do aplicativo Microsoft, use o seguinte comando se você estiver instalando ou atualizando para o cliente da área de trabalho do App-V 4.5 CU1:

    msiexec /i dw20shared.msi APPGUID={FE495DBC-6D42-4698-B61F-86E655E0796D}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

Como alternativa, se você estiver instalando ou atualizando para o App-V 4,5 CU1 o cliente de serviços de terminal, use o seguinte comando:

    msiexec /i dw20shared.msi APPGUID={8A97C241-D92A-47DC-B360-E716C1AAA929} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Observação**  O parâmetro APPGUID referencia o código do produto do cliente App-V do qual você instala ou atualiza. O código do produto é exclusivo para cada setup.msi. Você pode usar o editor de banco de dados Orca ou uma ferramenta semelhante para examinar os arquivos do Windows Installer e determinar o código do produto. Esta etapa é necessária para todas as instalações ou atualizações para o App-V 4.5 CU1.

 

### <a href="" id="some-applications-might-fail-to-install-during-the-monitoring-phase-when-sequencing-on-windows-7-beta--"></a>Alguns aplicativos podem falhar ao instalar durante a fase de monitoramento durante a sequenciamento no Windows7 beta

Ao sequenciar na versão beta do Windows7 ou em um computador com o Windows Installer 5.0, alguns aplicativos podem falhar ao instalar durante a fase de monitoramento.

WORKAROUNDYou deve conceder manualmente ao grupo todos permissões de controle total para a seguinte chave do registro:

    HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\SystemGuard

**Importante**  Você deve usar o botão **avançado** para definir a opção "incluir permissões hereditárias do pai deste objeto".

 

### Não é possível salvar pacotes durante a sequenciagem no Windows7 beta

Ao sequenciar no Windows7 beta, talvez você não consiga salvar o pacote sequenciado devido a uma violação de compartilhamento.

SOLUÇÕES alternativas especificadas na seção práticas recomendadas do guia de sequenciamento do Microsoft Application Virtualization 4.5 (consulte <https://go.microsoft.com/fwlink/?LinkId=144108> ), você deve desligar e desabilitar os seguintes programas de software antes de começar a sequenciamento:

-   Windows Defender

-   Software antivírus

-   Software de desfragmentação de disco

-   Windows Search

-   Qualquer sessão aberta do Windows Explorer

Além disso, se você tiver o Microsoft Update em execução na estação de sequenciamento para capturar atualizações durante o processo de atualização do pacote, será necessário adicionar "C:\\Windows\\SoftwareDistribution" como uma exclusão de VFS antes de iniciar o sequenciamento.

### Melhorar o desempenho ao sequenciar o .NET Framework

Ao sequenciar o .NET Framework, você pode enfrentar um desempenho de sistema reduzido porque o serviço NGEN do Microsoft .NET Framework tenta pré-compilar assemblies como uma tarefa em segundo plano.

WORKAROUNDWhen sequenciando o .NET Framework, desabilite o serviço NGEN do Microsoft .NET Framework (mscorsvw.exe) após concluir a fase de monitoramento. Você deve usar a guia de **Serviços virtuais** no sequenciador e alterar o tipo de inicialização para desabilitado.

### Problemas de interoperabilidade com a barra de tarefas do Windows7

Quando você executa o aplicativo cliente do Application Virtualization no Windows7, a barra de tarefas do Windows7 não recolhe várias instâncias de um aplicativo virtual em um único botão da barra de tarefas. Além disso, as listas de saltos não são exibidas quando você clica com o botão direito do mouse em um botão da barra de tarefas de um aplicativo virtual, a menos que o aplicativo tenha sido fixado na barra de tarefas do Windows7.

### Quando você desinstala o cliente do Microsoft Application Virtualization, as configurações do usuário associadas ao usuário que está realizando a desinstalação serão excluídas

Ao desinstalar o cliente do Microsoft Application Virtualization, o Windows Installer removerá as configurações do Application Virtualization do perfil do usuário atual. Se o seu computador usa perfis de roaming, não use sua conta de rede pessoal para desinstalar o cliente porque ele removerá as configurações de seus aplicativos virtuais em todos os seus computadores.

WORKAROUNDYou deve executar a desinstalação do cliente App-V com uma conta administrativa que não é usada para executar aplicativos virtuais.

### As edições feitas nas guias sistema de arquivos virtual e registro virtual devem ser salvas durante a execução do assistente de sequenciamento

Se você abrir um pacote para executar uma atualização ou já tiver executado o assistente de sequenciamento com um novo pacote e fizer alterações no pacote nas guias sistema de arquivos virtual ou registro virtual, essas alterações não serão salvas automaticamente.

WORKAROUNDSave as alterações antes de executar o assistente novamente para garantir que elas sejam refletidas dentro do ambiente virtual do assistente.

### O sequenciador de linha de comando deve ser executado em um prompt de comando elevado

Quando você usa o sequenciador de linha de comando, ele não solicita elevação.

WORKAROUNDRun o sequenciador de linha de comando usando um prompt de comando elevado.

### Configuração do console de gerenciamento do servidor em ambientes distribuídos

Se você precisar instalar os componentes de gerenciamento em sistemas diferentes do servidor principal de publicação e streaming do Application Virtualization, a instalação do servidor aceitará a instalação do nosso console de gerenciamento e do Web Service em servidores separados do servidor principal do Application Virtualization quando configurado corretamente.

Para distribuir os componentes de gerenciamento em vários servidores, a delegação Kerberos deve estar habilitada no servidor em que o serviço Web está instalado.

### Nomes de variáveis de caminho curto nos arquivos OSD podem causar erros

Se você receber o erro 450478-1F702339-0000010B "o nome do diretório é inválido" ao iniciar um aplicativo virtual no cliente, é possível que a variável no OSD esteja definida incorretamente. Isso pode acontecer se o instalador do aplicativo definir um nome de caminho curto durante o sequenciamento.

WORKAROUNDRemove o til à direita de qualquer variável CSIDl que exista no arquivo OSD.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Sintaxe correta para o parâmetro DECODEPATH para o sequenciador de linha de comando

No sequenciador de linha de comando, ao abrir um pacote para atualização e decodificá-lo na raiz da unidade Q, a sintaxe do parâmetro *DECODEPATH* não deve incluir uma barra à direita.

WORKAROUNDYou pode usar **Q:** em vez de **Q:\\** (omitindo o caractere "\ \" à direita).

### <a href="" id="when-upgrading-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Durante a atualização de pacotes 4.2, você encontra problemas causados por arquivos do Windows Installer no sistema de arquivos virtual

Ao atualizar um pacote do 4.2, você pode enfrentar problemas relacionados a uma incompatibilidade de arquivos de sistema do Windows Installer que foram incluídos por padrão no 4.2 e nas bibliotecas do Windows Installer instaladas localmente na sua estação de trabalho de sequenciamento. Os arquivos a seguir estão localizados em CSIDl \ _SYSTEM \ \:

cabinet.dll

msi.dll

msiexec.exe

msihnd.dll

msimsg.dlll

WORKAROUNDDelete todos os arquivos anteriores do pacote. Exclua os mapeamentos na guia **VFS** , bem como os arquivos reais na pasta CSIDL \ _SYSTEM em seu caminho de decodificação.

### <a href="" id="on-windows-xp--client-install-logging-is-not-enabled-by-default-"></a>No WindowsXP, o log de instalação do cliente não é habilitado por padrão

Ao instalar o cliente, para garantir que qualquer erro de instalação seja capturado para fins de solução de problemas, você deve habilitar o registro em log usando a linha de comando.

WORKAROUNDAdd o parâmetro */l\ * VX! log.txt* para a linha de comando, conforme mostrado no exemplo a seguir:

setup.exe/s/v "/qn/l\ * VX! log.txt "

msiexec.exe/i setup.msi/qn/l\ * VX! log.txt

Você também pode definir a chave do registro como o seguinte valor:

\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "logging" = "voicewarmupx!"

### Para que a autenticação Kerberos funcione, os SPNs (nomes principais de serviço) devem ser registrados para o IIS

Ao usar o IIS 6.0 ou 7.0 para o ícone ou a recuperação de arquivo do OSD e do streaming de pacotes, para que a autenticação Kerberos seja habilitada, os SPNs devem ser registrados da seguinte maneira:

-   No servidor IIS, execute os seguintes comandos usando a ferramenta kit de recursos do SETSPN.EXE. O nome de domínio totalmente qualificado do servidor (FQDN) deve ser usado.

    SetSPN-r SOFTGRID/ &lt; servidor FQDN&gt;

    SetSPN-r HTTP/ &lt; servidor FQDN&gt;

Para obter mais informações, consulte <https://go.microsoft.com/fwlink/?LinkId=131407> .

### Na atualização do RC, as permissões padrão nos logs do cliente não permitem que os usuários que não são administradores acessem os logs para solução de problemas e suporte.

As permissões padrão nos logs do cliente para o aplicativo VirtualizationRC cliente não permitia o acesso não administrador a arquivos de log e alterações manuais nessas permissões de log foram revertidas quando os clientes foram reiniciados. Isso foi corrigido na versão RTM para instalações de novos clientes, mas na atualização do RC, as permissões personalizadas em arquivos de log existentes não são redefinidas. No entanto, quando novos logs são criados ou após uma redefinição de log, os arquivos terão as novas permissões padrão.

WORKAROUNDAfter a atualização, redefina os logs de cliente existentes ou altere manualmente as permissões deles.

### Alterações de compatibilidade do .NET

O Update1 cumulativo do Microsoft Application Virtualization suporta o sequenciamento do .NET Framework no WindowsXP (SP2 ou posterior). As rotinas de sequenciamento para aplicativos .NET que foram escritas para o SoftGrid 4.2 podem precisar ser atualizadas quando usadas com o sequenciador App-V 4.5. Para obter detalhes e soluções alternativas, consulte o artigo da base de dados de conhecimento em <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Após a atualização do cliente do App-V 4.2, alguns aplicativos não são mostrados

Verifique o seguinte erro no log: "o cliente do Application Virtualization não pôde analisar o arquivo OSD". O cliente do Microsoft Application Virtualization 4.5 filtra os aplicativos que têm um arquivo OSD contendo uma marca de sistema operacional vazia ( &lt; &gt; &lt; /os &gt; ).

WORKAROUNDDelete a marca de sistema operacional vazia do arquivo OSD.

### O servidor App-V requer isenções no firewall para certos processos

Para que o servidor transmita os aplicativos corretamente, os processos principais do servidor, incluindo o Dispatcher, precisam de acesso por meio do firewall.

Isenções de contorno no firewall do servidor para os seguintes processos: sghwsvr.exe e sghwdsptr.exe. Isso se aplica ao servidor de gerenciamento do App-V e ao App-V Streaming Server.

### Os pacotes de sequenciamento que exigem novos tempos de execução do Visual Basic podem falhar

Se você sequenciar um pacote que usa uma versão mais recente de um tempo de execução do Visual Basic (VB) em um sistema em que uma versão mais antiga do VBruntime está instalada, talvez você veja uma falha ou outro comportamento inesperado ao tentar usar seu pacote. Por exemplo, se você tentar sequenciar o Microsoft Money2007, que usa a versão 6.00.9782 do VBruntime, em um sistema WindowsXP com a versão 6.00.9690 do VBruntime, talvez veja uma falha no designer de faturas quando você tenta executá-lo em outro sistema WindowsXP com o VBruntime mais antigo.

WORKAROUNDAfter de instalar o aplicativo no computador de sequenciamento, e ainda monitorar, copie o VBruntime correto (mais recente) para o diretório no pacote do qual o executável foi iniciado. Isso permite que o aplicativo sequenciado encontre a versão esperada do VBruntime quando ele é iniciado.

**Importante**  Esse problema foi corrigido no Update1 cumulativo do Microsoft Application Virtualization 4.5.

 

### Quando o instalador do servidor é executado no modo silencioso, ele não verifica corretamente se o MSXML6

O servidor de gerenciamento do App-V depende do MSXML6. No entanto, se você executar o instalador no modo silencioso, por exemplo, usando o comando "msiexec-i setup.msi/qn" em um sistema em que o MSXML6 ainda não está instalado, o instalador não verá a dependência ausente e instalará de qualquer forma. O resultado mais comum é que, quando os clientes tentam atualizar as informações de publicação do servidor de gerenciamento do App-V, eles verão falhas.

WORKAROUNDVerify que o MSXML6 está instalado no sistema antes de tentar uma instalação silenciosa do servidor de gerenciamento do App-V.

### Código de erro 000C800 ao tentar se conectar ao console de gerenciamento do Application Virtualization

Um administrador de virtualização de aplicativos que não seja um administrador local no servidor do serviço de gerenciamento do Application Virtualization receberá um erro (código de erro: 000C800) ao tentar se conectar ao console de gerenciamento do Application Virtualization, e a entrada SftMMC. log indicará que o acesso a SftMgmt. udl será negado. Para conectar-se com êxito ao console de gerenciamento do Application Virtualization, um administrador de virtualização de aplicativos que não seja um administrador local no servidor do serviço de gerenciamento do Application Virtualization deve ter pelo menos acesso de leitura e execução ao arquivo SftMgmt. udl.

Os administradores de virtualização de aplicativos devem receber permissões de leitura e execução para o arquivo SftMgmt. UDL em%systemdrive%\\Program Files\\Microsoft System Center App Virt Management Server\\App Service Management Service.

### Parâmetros de linha de comando do instalador do cliente são ignorados quando usados em conjunto com KEEPCURRENTSETTINGS = 1

Quando usado em conjunto com KEEPCURRENTSETTINGS = 1, os seguintes parâmetros de linha de comando do instalador do cliente são ignorados: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA e REQUIRESECURECONNECTION.

WORKAROUNDIf você tiver configurações que deseja manter, use KEEPCURRENTSETTINGS = 1 e, em seguida, defina os outros parâmetros após a implantação. O modelo App-V ADM pode ser usado para definir as seguintes configurações de cliente: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES e ALLOWINDEPENDENTFILESTREAMING. O modelo ADM pode ser encontrado em <https://go.microsoft.com/fwlink/?LinkId=121835> .

### Erro ao inicializar aplicativos virtuais com o Symantec Endpoint Protection

Ao usar o Symantec Endpoint Protection com o recurso de controle de aplicativo e dispositivo habilitado, os aplicativos virtuais podem falhar ao iniciar, com o erro "o aplicativo não pôde ser inicializado corretamente (0xc000007b)". Para obter detalhes e soluções alternativas, consulte o artigo da base de dados de conhecimento em <https://go.microsoft.com/fwlink/?LinkId=125851> .

**Importante**  Esse problema foi corrigido no Update1 cumulativo do Microsoft Application Virtualization 4.5.

 

## Informações de direitos autorais da versão


As informações contidas neste documento, incluindo URL e outras referências de site da Web na Internet, estão sujeitas a alterações sem aviso prévio e são fornecidas apenas para fins informativos. Todo o risco do uso ou dos resultados do uso deste documento permanece com o usuário, e a Microsoft Corporation não oferece nenhuma garantia, seja expressa ou implícita. Os exemplos de empresas, organizações, produtos, pessoas e eventos descritos aqui são fictícios. Nenhuma associação com qualquer empresa, organização, produto, pessoa ou evento real é intencional ou deve ser inferida. Obedecer a todas as leis de direitos autorais aplicáveis é responsável pelo usuário. Sem limitar os direitos sob direitos autorais, nenhuma parte deste documento pode ser reproduzida, armazenada ou introduzida em um sistema de recuperação, ou transmitida de qualquer forma ou por qualquer meio (eletrônico, mecânico, fotocópia, gravação ou de outra forma) ou para qualquer propósito, sem a permissão expressa por escrito da Microsoft Corporation.

A Microsoft pode ter patentes, aplicativos de patente, marcas comerciais, direitos autorais ou outros direitos de propriedade intelectual que abranjam o assunto deste documento. Exceto conforme expressamente fornecido em qualquer contrato de licença escrito da Microsoft, o fornecimento deste documento não lhe concede nenhuma licença para essas patentes, marcas comerciais, direitos autorais ou outra propriedade intelectual.



Microsoft, MS-DOS, Windows, WindowsServer, Windows Vista, Active Directory e ActiveSync são marcas registradas ou marcas comerciais da MicrosoftCorporation nos Estados Unidos e/ou em outros países.

Os nomes das empresas e produtos reais mencionados aqui podem ser marcas comerciais de seus respectivos proprietários.

 

 





