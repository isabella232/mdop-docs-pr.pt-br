---
title: Notas da versão do sistema de gerenciamento do Microsoft Application Virtualization 4,5 SP1
description: Notas da versão do sistema de gerenciamento do Microsoft Application Virtualization 4,5 SP1
author: dansimp
ms.assetid: 5d6b11ea-7b87-4084-9a7c-0d831f247aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c24d2e98ad09460ca22e4b29d75ae2b9c72d0bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796869"
---
# Notas da versão do sistema de gerenciamento do Microsoft Application Virtualization 4,5 SP1


Para pesquisar essas notas de versão, pressione CTRL + F.

**Importante**  Leia estas notas de versão cuidadosamente antes de instalar o sistema de gerenciamento do Application Virtualization. Estas notas da versão contêm informações que você precisa para instalar o sistema de gerenciamento do Application Virtualization com êxito. Estas notas da versão contêm informações que não estão disponíveis na documentação do produto. Se houver discrepância entre essas notas de versão e outras documentações do sistema de gerenciamento do aplicativo Virtualization, a alteração mais recente deve ser considerada autorizada.

 

Para obter informações atualizadas sobre problemas conhecidos, acesse a biblioteca do Microsoft TechNet em <https://go.microsoft.com/fwlink/?LinkId=122918> .

## Sobre o Microsoft Application Virtualization 4,5 Service Pack 1


Estas notas de versão foram atualizadas para refletir as alterações introduzidas com o Microsoft Application Virtualization (App-V) 4.5 Service Pack1 (SP1). Este Service Pack contém as seguintes alterações:

-   Suporte para o Windows 7 e o Windows Server 2008 R2: o App-V 4,5 SP1 oferece suporte para o Windows 7 e o Windows Server 2008 R2, incluindo suporte para recursos do Windows 7, como a barra de tarefas, o AppLocker, o BranchCache e o BitLocker To Go.O suporte do Windows Server 2008 R2 é somente para o servidor do Application Virtualization. Para obter mais informações sobre o suporte do AppLocker no Windows 7, consulte <https://go.microsoft.com/fwlink/?LinkID=156732> .

-   Suporte para territórios Kerberos de terceiros: App-V 4,5 SP1 fornece suporte para ambientes que têm uma relação de confiança e contas de usuário mapeadas entre um domínio do Windows e um realm Kerberos de MIT, que é um cenário comum em muitas universidades. Para saber mais sobre como habilitar esse suporte, acesse a biblioteca do Microsoft TechNet em <https://go.microsoft.com/fwlink/?LinkId=166004> .

-   Suporte aprimorado para publicação de aplicativos e streaming via HTTP/HTTPS: App-V 4,5 SP1 fornece suporte para publicação de aplicativos e streaming via protocolos HTTP/HTTPS para Windows XP Home Edition, Windows Vista Home Basic e Windows 7 Home Basic.

-   Feedback do cliente e pacote cumulativo de hotfix: App-V 4.5 SP1 também inclui um acúmulo de correções para solucionar problemas encontrados desde o lançamento do Microsoft Application Virtualization (App-V) 4.5 CU1. As atualizações são resultado de uma combinação de problemas conhecidos e comentários dos clientes de nossas equipes, parceiros e clientes que usam o App-V 4.5. Para obter uma lista completa das atualizações, consulte o artigo da base de conhecimento em <https://go.microsoft.com/fwlink/?LinkId=167121> .

## Sobre a documentação do produto


A documentação abrangente da virtualização de aplicativos (App-V) está disponível no Microsoft TechNet no TechCenter Application Virtualization (App-V) em <https://go.microsoft.com/fwlink/?LinkId=122939> . A documentação do TechNet inclui a ajuda online para o Application Virtualization Sequencer, o cliente Application Virtualization e o servidor Application Virtualization. Ele também inclui o guia de planejamento e implantação do Application Virtualization e o guia de operações de virtualização de aplicativo.

## Proteger contra vulnerabilidades e vírus de segurança


Para ajudar a proteger contra vulnerabilidades e vírus de segurança, recomendamos que você instale as últimas atualizações de segurança disponíveis para qualquer novo software sendo instalado. Para obter mais informações, consulte o site de segurança da Microsoft em <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Como fornecer comentários


Você pode enviar comentários, fazer uma sugestão ou relatar um problema com o sistema de gerenciamento do Microsoft Application Virtualization (App-V) por meio de um fórum da Comunidade no Microsoft Application Virtualization TechCenter ( <https://go.microsoft.com/fwlink/?LinkId=122917> ).

Você também pode fornecer seus comentários sobre a documentação diretamente para a equipe de documentação do App-V. Envie seus comentários sobre a documentação para appvdocs@microsoft.com.

## Problemas conhecidos do Application Virtualization 4.5 SP1


Esta seção fornece as informações mais atualizadas sobre problemas com o Microsoft Application Virtualization (App-V) 4.5 SP1. Esses problemas não aparecem na documentação do produto e, em alguns casos, podem participar da documentação existente do produto. Sempre que possível, esses problemas serão abordados em lançamentos posteriores do software.

### Orientação para instalar o console de gerenciamento do servidor

Se você precisar instalar o software de gerenciamento em sistemas diferentes do servidor principal de publicação e streaming do Application Virtualization, a instalação do servidor oferece suporte à instalação do console de gerenciamento e do serviço Web de gerenciamento em servidores separados do servidor de gerenciamento do App-V primário. Para distribuir os componentes de gerenciamento em vários servidores, a delegação Kerberos deve estar habilitada no servidor em que o serviço Web está instalado. Para saber mais sobre como habilitar esse suporte, acesse a biblioteca do Microsoft TechNet em <https://go.microsoft.com/fwlink/?LinkId=166682>

### Orientação para instalar ou atualizar clientes para o App-V 4.5 SP1 usando o setup.msi

Ao instalar ou atualizar seus clientes do App-V para o App-V 4,5 SP1 usando setup.msi, os pré-requisitos não são instalados automaticamente.

O WORKAROUNDYou deve instalar manualmente os pré-requisitos antes de instalar ou atualizar o aplicativo App-V cliente toApp-V 4,5 SP1. Para obter procedimentos detalhados de instalação dos pré-requisitos e do cliente App-V, consulte <https://go.microsoft.com/fwlink/?LinkId=144106> .

Quando isso tiver sido concluído, instale o cliente App-V 4,5 SP1 usando setup.msi com privilégios elevados. Esse arquivo está disponível na mídia de versão do App-V 4,5 SP1 na pasta Installers\\Client

Ao instalar o relatório de erros do aplicativo Microsoft, use o seguinte comando se você estiver instalando ou atualizando para o cliente da área de trabalho do App-V 4,5 SP1:

    msiexec /i dw20shared.msi APPGUID={93468B43-C19D-44F9-8BCC-114076DB0443}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

Como alternativa, se você estiver instalando ou atualizando para o cliente do App-V 4,5 SP1 para serviços de área de trabalho remota (antes serviços de terminal), use o seguinte comando:

    msiexec /i dw20shared.msi APPGUID={0042AD3C-99A4-4E58-B5F0-744D5AD96E1C} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Observação**  O parâmetro APPGUID referencia o código do produto do cliente App-V que você instala ou atualiza. O código do produto é exclusivo para cada setup.msi. Você pode usar o editor de banco de dados Orca ou uma ferramenta semelhante para examinar os arquivos do Windows Installer e determinar o código do produto. Esta etapa é necessária para todas as instalações ou atualizações para o App-V 4,5 SP1.

 

### Melhorar o desempenho ao sequenciar o .NET Framework

Ao sequenciar o .NET Framework, você pode enfrentar um desempenho de sistema reduzido porque o serviço NGEN do Microsoft .NET Framework tenta pré-compilar assemblies como uma tarefa em segundo plano.

WORKAROUNDWhen sequenciando o .NET Framework, desabilite o serviço NGEN do Microsoft .NET Framework (mscorsvw.exe) após concluir a fase de monitoramento. Você deve usar a guia de **Serviços virtuais** no sequenciador e alterar o tipo de inicialização para desabilitado.

### Quando você desinstala o cliente do Microsoft Application Virtualization, as configurações do usuário associadas ao usuário que está realizando a desinstalação serão excluídas

Ao desinstalar o cliente App-V, o Windows Installer removerá as configurações do Application Virtualization do perfil do usuário atual. Se o seu computador usa perfis de roaming, não use sua conta de rede pessoal para desinstalar o cliente porque ele removerá as configurações de seus aplicativos virtuais em todos os seus computadores.

WORKAROUNDYou deve executar a desinstalação do cliente App-V com uma conta administrativa que não é usada para executar aplicativos virtuais.

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

### Alterações de compatibilidade do .NET

O Update1 cumulativo do Microsoft Application Virtualization (App-V) cumulativo ou posterior dá suporte ao sequenciamento do .NET Framework no WindowsXP (SP2 ou posterior). As rotinas de sequenciamento para aplicativos .NET que foram escritos para o SoftGrid 4.2 podem precisar ser atualizadas quando usadas com o sequenciador do App-V 4,5. Para obter detalhes e soluções alternativas, consulte o artigo da base de dados de conhecimento em <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Após a atualização do cliente do App-V 4.2, alguns aplicativos não são mostrados

Verifique o seguinte erro no log: "o cliente do Application Virtualization não pôde analisar o arquivo OSD". O cliente App-V 4,5 filtra os aplicativos que têm um arquivo OSD contendo uma marca de sistema operacional vazia ( &lt; os &gt; &lt; /os &gt; ).

WORKAROUNDDelete a marca de sistema operacional vazia do arquivo OSD.

### O servidor App-V requer isenções no firewall para certos processos

Para que o servidor transmita os aplicativos corretamente, os processos principais do servidor, incluindo o Dispatcher, precisam de acesso por meio do firewall.

Isenções de contorno no firewall do servidor para os seguintes processos: sghwsvr.exe e sghwdsptr.exe. Isso se aplica ao servidor de gerenciamento do App-V e ao App-V Streaming Server.

### Quando o instalador do servidor é executado no modo silencioso, ele não verifica corretamente se o MSXML6

O servidor de gerenciamento do App-V depende do MSXML6. No entanto, se você executar o instalador no modo silencioso, por exemplo, usando o comando "msiexec-i setup.msi/qn" em um sistema em que o MSXML6 ainda não está instalado, o instalador não detecta a dependência ausente e instala assim mesmo. Portanto, quando os clientes tentam atualizar as informações de publicação do servidor de gerenciamento do App-V, eles verão falhas.

WORKAROUNDVerify que o MSXML6 está instalado no sistema antes de tentar uma instalação silenciosa do servidor de gerenciamento do App-V.

### Código de erro 000C800 ao tentar se conectar ao console de gerenciamento do Application Virtualization

Um administrador de virtualização de aplicativos que não seja um administrador local no servidor de serviço Web de gerenciamento do App-V receberá um erro (código de erro: 000C800) ao tentar se conectar ao console de gerenciamento do App-V, e a entrada SftMMC. log indicará que o acesso a SftMgmt. udl foi negado. Para conectar-se com êxito ao console de gerenciamento do App-V, um administrador que não tem direitos de administrador local no servidor de serviço Web de gerenciamento do App-V deve ter pelo menos permissões de leitura e execução para o arquivo SftMgmt. udl.

Os administradores de virtualização de aplicativos devem receber permissões de leitura e execução para o arquivo SftMgmt. UDL em%systemdrive%\\Program Files\\Microsoft System Center App Virt Management Server\\App Service Management Service.

### Parâmetros de linha de comando do instalador do cliente são ignorados quando usados em conjunto com KEEPCURRENTSETTINGS = 1

Quando usado em conjunto com KEEPCURRENTSETTINGS = 1, os seguintes parâmetros de linha de comando do instalador do cliente são ignorados: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA e REQUIRESECURECONNECTION.

WORKAROUNDIf você tiver configurações que deseja manter, use KEEPCURRENTSETTINGS = 1 e, em seguida, defina os outros parâmetros após a implantação. O modelo App-V ADM pode ser usado para definir as seguintes configurações de cliente: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES e ALLOWINDEPENDENTFILESTREAMING. O modelo ADM pode ser encontrado em <https://go.microsoft.com/fwlink/?LinkId=121835> .

## Informações de direitos autorais da versão


As informações contidas neste documento, incluindo URL e outras referências de site da Web na Internet, estão sujeitas a alterações sem aviso prévio e são fornecidas apenas para fins informativos. Todo o risco do uso ou dos resultados do uso deste documento permanece com o usuário, e a Microsoft Corporation não oferece nenhuma garantia, seja expressa ou implícita. Salvo indicação em contrário, as empresas, organizações, produtos, nomes de domínio, endereços de email, logotipos, pessoas, lugares e eventos descritos nos exemplos aqui são fictícios. Nenhuma associação com qualquer empresa, organização, produto, nome de domínio, endereço de email, logotipo, pessoa, lugar ou evento real é intencional ou deve ser inferida. Obedecer a todas as leis de direitos autorais aplicáveis é responsável pelo usuário. Sem limitar os direitos sob direitos autorais, nenhuma parte deste documento pode ser reproduzida, armazenada ou introduzida em um sistema de recuperação, ou transmitida de qualquer forma ou por qualquer meio (eletrônico, mecânico, fotocópia, gravação ou de outra forma) ou para qualquer propósito, sem a permissão expressa por escrito da Microsoft Corporation.

A Microsoft pode ter patentes, aplicativos de patente, marcas comerciais, direitos autorais ou outros direitos de propriedade intelectual que abranjam o assunto deste documento. Exceto conforme expressamente fornecido em qualquer contrato de licença escrito da Microsoft, o fornecimento deste documento não lhe concede nenhuma licença para essas patentes, marcas comerciais, direitos autorais ou outra propriedade intelectual.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer e Windows Vista são marcas comerciais do grupo de empresas da Microsoft.

Todas as outras marcas comerciais são propriedade de seus respectivos proprietários.

 

 





