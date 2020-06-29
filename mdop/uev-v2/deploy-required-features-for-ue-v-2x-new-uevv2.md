---
title: Implantar os recursos necessários na UE-V 2.x
description: Implantar os recursos necessários na UE-V 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799518"
---
# Implantar os recursos necessários na UE-V 2.x


Todas as implantações do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 exigem estes recursos

-   [Implante um local de armazenamento de configurações](#ssl) acessível para os usuários finais.

    Esse é um compartilhamento de rede padrão que armazena e recupera configurações de usuário.

-   [Escolher o método de configuração para UE-V](#config)

    O UE-V pode ser implantado e configurado com ferramentas comuns de gerenciamento, como política de grupo, configuração do Configuration Manager ou infraestrutura de gerenciamento do Windows e PowerShell.

-   [Implante um agente do UE-V](#agent) para ser instalado em cada computador que sincroniza as configurações.

    Isso monitora os aplicativos registrados e o sistema operacional em busca de alterações de configurações e sincroniza essas configurações entre computadores.

Os tópicos desta seção descrevem como implantar esses recursos.

## <a href="" id="ssl"></a>Implantar um local de armazenamento de configurações do UE-V


O UE-V exige um local no qual armazenar configurações de usuário em arquivos de pacote de configurações. Você pode definir esse local de armazenamento de configurações de uma destas maneiras:

-   Criar seu próprio local de armazenamento de configurações

-   Usar o Active Directory existente para o local de armazenamento de configurações

Se você não criar um local de armazenamento de configurações, o UE-V Agent usará o Active Directory (AD) por padrão.

**Observação**  
Em questão de [desempenho e planejamento de capacidade](https://technet.microsoft.com/library/dn458932.aspx#capacity) e para reduzir problemas com a latência da rede, crie locais de armazenamento de configurações nas mesmas redes locais em que os computadores dos usuários residem. Recomendamos 20 MB de espaço em disco por usuário para o local de armazenamento de configurações.



### Criar um local de armazenamento de configurações do UE-V

Antes de definir o local de armazenamento de configurações, você deve criar um diretório raiz com permissões de leitura/gravação para usuários que armazenam configurações no compartilhamento. O UE-V Agent cria pastas específicas do usuário neste diretório raiz.

O local de armazenamento de configurações é definido definindo a opção de configuração SettingsStoragePath, que você pode configurar usando um destes métodos:

-   Ao [implantar o UE-V Agent](#agent) por meio de um parâmetro de linha de comando ou em um script em lotes

-   Por meio das configurações de [política de grupo](https://technet.microsoft.com/library/dn458893.aspx)

-   Com o [pacote de configuração do System Center](https://technet.microsoft.com/library/dn458917.aspx) para UE-V

-   Após a instalação do UE-V Agent, usando o [Windows PowerShell ou WMI (Instrumentação de gerenciamento do Windows)](https://technet.microsoft.com/library/dn458937.aspx)

O caminho deve estar em um caminho UNC (Convenção Universal de nomenclatura) do servidor e do compartilhamento. Por exemplo, **\\\\Server\\Settingsshare\\**. Essa opção de configuração oferece suporte ao uso de variáveis para habilitar cenários de sincronização específicos. Por exemplo, você pode usar as `%username%\%computername%` variáveis para preservar a experiência das configurações do usuário final nos seguintes cenários:

-   Usuários finais que usam vários computadores físicos em sua empresa

-   Computadores corporativos que são usados por vários usuários finais

O UE-V Agent cria dinamicamente um caminho de armazenamento de configurações específico do usuário, com uma pasta de sistema oculta nomeada `SettingsPackages` , com base na configuração de configuração de **SettingsStoragePath**. O agente lê e grava as configurações nesse local conforme definido pelos modelos de localização de configurações do UE-V registrados.

**As configurações de UE-V são determinadas por uma regra "última gravação de WINS":** Se o local de armazenamento de configurações for o mesmo para usuários com vários computadores gerenciados, um agente UE-V lê e grava no local de configurações independentemente dos agentes em execução em outros computadores. As configurações e os valores gravados por último são aqueles aplicados quando o próximo agente lê do local de armazenamento de configurações.

**Implantar o local de armazenamento de configurações:** Siga estas etapas para definir o local de armazenamento de configurações em vez de usar o serviço existente do Active Directory. Você deve limitar o acesso ao compartilhamento de armazenamento de configurações a esses usuários que precisam dele, conforme mostrado nas tabelas abaixo.

**Para implantar o compartilhamento de rede UE-V**

1.  Crie um novo grupo de segurança para usuários do UE-V.

2.  Crie uma nova pasta no computador centralizado que armazena os pacotes de configurações do UE-V e conceda aos usuários do UE-V acesso às permissões de grupo para a pasta. O administrador que dá suporte a UE-V deve ter permissões para esta pasta compartilhada.

3.  Defina as seguintes permissões de bloco de mensagens de servidor (SMB) de nível de compartilhamento para a pasta de local de armazenamento de configurações.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Conta de usuário</strong></th>
    <th align="left"><strong>Permissões recomendadas</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>Nenhuma permissão</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Grupo de segurança de usuários do UE-V</p></td>
    <td align="left"><p>Controle total</p></td>
    </tr>
    </tbody>
    </table>



4.  Defina as seguintes permissões do sistema de arquivos NTFS para a pasta de local de armazenamento de configurações.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Conta de usuário</strong></th>
    <th align="left"><strong>Permissões recomendadas</strong></th>
    <th align="left"><strong>Pasta</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Criador/proprietário</p></td>
    <td align="left"><p>Controle total</p></td>
    <td align="left"><p>Somente subpastas e arquivos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Grupo de segurança de usuários do UE-V</p></td>
    <td align="left"><p>Listar pasta/ler dados, criar pastas/acrescentar dados</p></td>
    <td align="left"><p>Somente esta pasta</p></td>
    </tr>
    </tbody>
    </table>



Com essa configuração, o UE-V Agent cria e protege uma pasta Settingspackage enquanto ele é executado no contexto do usuário e concede a cada usuário permissão para criar pastas para armazenamento de configurações. Os usuários recebem controle total para a pasta Settingspackage enquanto outros usuários não podem acessá-lo.

**Observação**  
Se você criar o compartilhamento de armazenamento configurações em um computador que esteja executando um sistema operacional Windows Server, configure o UE-V para verificar se o grupo Administradores local ou o usuário atual é o proprietário da pasta em que os pacotes de configurações estão armazenados. Para habilitar essa segurança adicional, especifique essa configuração no editor do registro do Windows Server:

1.  Adicione uma chave do registro **reg \ _DWORD** chamada **"RepositoryOwnerCheckEnabled"** ao **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Defina o valor da chave do registro como *1*.



### Usar o Active Directory com o UE-V 2. x

Por padrão, o UE-V Agent usa o Active Directory (AD) se um local de armazenamento de configurações não for definido de outra forma. Nesses casos, o UE-V Agent cria dinamicamente a pasta de armazenamento de configurações na raiz do diretório base do AD de cada usuário. Mas, se uma configuração de diretório personalizada estiver configurada no AD, esse diretório será usado em vez disso.

## <a href="" id="config"></a>Escolha o método de configuração para UE-V 2. x


Você deseja descobrir qual método de configuração será usado para gerenciar o UE-V após a implantação, pois esse será o método de configuração usado para implantar o UE-V Agent. Geralmente, esse é o método de configuração que você já usa em seu ambiente, como o Windows PowerShell ou o Configuration Manager.

Você pode configurar o UE-V antes, durante ou após a instalação do UE-V Agent, dependendo do método de configuração que você usa.

-   [Política de grupo](https://technet.microsoft.com/library/dn458893.aspx)**:** você pode usar sua infraestrutura de política de grupo existente para configurar o UE-v antes ou depois da implantação do agente do UE-v. O modelo ADMX da política de grupo UE-V permite o gerenciamento centralizado das opções de configuração comuns do agente do UE-V e inclui configurações para configurar a sincronização de UE-V.

    **Instalando os modelos ADMX da política de grupo UE-V:** Modelos ADMX de política de grupo para UE-V defina as configurações de sincronização para o UE-V Agent e habilite o gerenciamento centralizado das configurações comuns de configuração do agente do UE-V usando uma infraestrutura de política de grupo existente.

    Os sistemas operacionais com suporte para o controlador de domínio que implanta os objetos de política de grupo incluem o seguinte:

    Windows Server 2008 R2

    Windows Server 2012 e Windows Server 2012 R2

-   [Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** o pacote de configuração do UE-V permite que você use o recurso configurações de conformidade do System Center Configuration Manager 2012 SP1 ou posterior para aplicar configurações consistentes entre sites nos quais o UE-V e o Configuration Manager estão instalados.

-   [Windows PowerShell e WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** você pode usar comandos com script para Windows PowerShell e Windows Management Instrumentation (WMI) para modificar as configurações depois de instalar o UE-V Agent.

    **Observação**  
    A modificação do registro pode resultar em perda de dados ou o computador deixa de responder. Recomendamos que você use outros métodos de configuração.



-   **Instalação de linha de comando ou de script em lotes:** Parâmetros que são usados quando você [implanta o UE-V Agent](#agent) define muitas configurações de UE-v. Sistemas de distribuição de software eletrônico, como o System Center 2012 Configuration Manager, usam esses parâmetros para configurar seus clientes ao implantar e instalar o software do agente do UE-V.

## <a href="" id="agent"></a>Implantar o agente UE-V 2. x


O UE-V Agent é o núcleo de uma implantação do UE-V e deve ser executado em cada computador que usa o UE-V para sincronizar as configurações do aplicativo e do Windows.

**Arquivos de instalação do UE-V Agent:** Um único arquivo de instalação, AgentSetup.exe, instala o UE-V Agent nos sistemas operacionais de 32 bits e 64 bits. Além disso, AgentSetupx86.msi ou arquivos do Windows Installer específicos da arquitetura do AgentSetupx64.msi são fornecidos e, como são menores, eles podem simplificar as implantações do agente. Os [parâmetros de linha de comando para o instalador do AgentSetup.exe](#params) também têm suporte para a instalação do Windows Installer.

**Importante**  
Durante a instalação ou desinstalação do agente do UE-V, você pode usar o arquivo AgentSetup.exe ou o &lt; arquivo AgentSetup Arch &gt; . msi, mas não ambos. O mesmo arquivo deve ser usado para desinstalar o UE-V Agent usado para instalar o UE-V Agent.



### Para implantar o UE-V Agent

Você pode usar os seguintes métodos para implantar o UE-V Agent:

-   Um sistema de solução ESD (Electronic Software Distribution), como o Configuration Manager, que pode instalar um arquivo Windows Installer (. msi).

-   Um script de instalação que faz referência ao arquivo do Windows Installer (. msi) que está armazenado centralmente em um compartilhamento.

-   Um programa de instalação que você executa manualmente no computador.

Use o procedimento a seguir para implantar o UE-V Agent de um compartilhamento de rede.

**Para instalar e configurar o UE-V Agent a partir de um compartilhamento de rede**

1.  Testar o arquivo de instalação do agente do UE-V AgentSetup.exe em um compartilhamento de rede ao qual os usuários têm permissão de leitura.

2.  Implante um script para os computadores dos usuários que instalam o UE-V Agent. O script deve especificar o local de armazenamento de configurações.

**Opções de implantação:** Certifique-se de usar o formato de variável correto ao instalar o UE-V Agent. A tabela a seguir fornece exemplos de opções de implantação para usar os arquivos AgentSetup.exe ou Windows Installer (. msi).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Tipo de implementação</strong></th>
<th align="left"><strong>Descrição da implantação</strong></th>
<th align="left"><strong>Exemplo</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Prompt de comando</p></td>
<td align="left"><p>Ao instalar o UE-V Agent em um prompt de comando, use o <em> formato de variável% ^ username% </em> . Se forem necessárias aspas por causa de espaços no caminho de armazenamento de configurações, use um arquivo de script em lotes para implantação.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Script em lotes</p></td>
<td align="left"><p>Ao instalar o UE-V Agent a partir de um arquivo de script em lotes, use o <em> formato de variável%% username%% </em> . Se você usar esse método de instalação, deverá escapar a variável com os caracteres%%. Sem esse caractere, o script expande a <em> </em> variável username no momento da instalação, em vez do tempo de execução, que faz com que o UE-V use um único local de armazenamento de configurações para todos os usuários.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell</p></td>
<td align="left"><p>Ao instalar o UE-V Agent a partir de um prompt do Windows PowerShell ou de um script do Windows PowerShell, use o <em> formato de variável% username% </em> .</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribuição de software eletrônico, como a implantação da implantação de software do Configuration Manager</p></td>
<td align="left"><p>Ao instalar o UE-V Agent usando o Configuration Manager, use o <em> formato de variável ^% username ^% </em> .</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**Observação**  
A instalação do UE-V Agent exige direitos de administrador, e o computador requer uma reinicialização para que o UE-V Agent possa ser executado.



### <a href="" id="params"></a>Parâmetros de linha de comando para implantação do agente UE-V

Os parâmetros de linha de comando do UE-V Agent são os seguintes.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Parâmetro de linha de comando</strong></th>
<th align="left"><strong>Definição</strong></th>
<th align="left"><strong>Observações</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help ou/h ou/?</p></td>
<td align="left"><p>Exibe a caixa de diálogo AgentSetup.exe uso.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Indica o caminho UNC (Convenção Universal de nomenclatura) que define onde as configurações são armazenadas.</p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Você deve especificar um SettingsStoragePath no UE-V 2,1 e no UE-V 2,1 SP1. Você pode definir a cadeia de caracteres AdHomePath para especificar que o caminho inicial do usuário&#39;s do Active Directory seja usado. Por exemplo, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</p>
<p>No UE-V 2,0, você pode deixar o SettingsStoragePath em branco para usar o caminho inicial do Active Directory.</p>
</div>
<div>

</div>
<p>as variáveis de ambiente% username% ou% computernamename% são aceitas. O script pode exigir variáveis de escape.</p>
<p><strong>Padrão </strong> : &lt; nenhum&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsStoragePathReg</p></td>
<td align="left"><p>Obtém o valor SettingsStoragePath do registro durante a instalação.</p></td>
<td align="left"><p>No prompt de comando, digite o exemplo a seguir para forçar o UE-V a usar o caminho inicial do Active Directory em vez de um UNC específico.</p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Indica o caminho UNC (Convenção Universal de nomenclatura) que define o local verificado para novos modelos de local de configurações.</p></td>
<td align="left"><p>Só é necessário para modelos de local de configurações personalizadas</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Especifica se os modelos padrão da Microsoft devem ser registrados durante a instalação.</p></td>
<td align="left"><p>Verdadeiro | Falsas</p>
<p><strong>Padrão </strong> : verdadeiro</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncMethod</p></td>
<td align="left"><p>Especifica qual método de sincronização deve ser usado.</p></td>
<td align="left"><p>SyncProvider | Nenhuma</p>
<p><strong>Padrão </strong> : SyncProvider</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Especifica o número de milissegundos que o computador aguarda antes do tempo limite quando ele recupera as configurações de usuário do local de armazenamento de configurações.</p></td>
<td align="left"><p><strong>Padrão </strong> : 2000 milissegundos</p>
<p>(Aguarde até 2 segundos)</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Especifica se a sincronização de UE-V está habilitada ou desabilitada.</p></td>
<td align="left"><p>Verdadeiro | Falsas</p>
<p><strong>Padrão </strong> : verdadeiro</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Especifica um tamanho de arquivo de pacote de configurações em bytes quando o UE-V Agent informa que os arquivos excedem o limite.</p></td>
<td align="left"><p>&lt;tamanho&gt;</p>
<p><strong>Padrão </strong> : nenhum (sem limite de aviso)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Especifica a configuração de participação no programa de aperfeiçoamento da experiência do usuário. Se definido como <strong> true </strong> , as informações do instalador serão carregadas no site do programa de aperfeiçoamento da experiência do usuário da Microsoft. Se definido como <strong> false </strong> , nenhuma informação será carregada.</p></td>
<td align="left"><p>Verdadeiro | Falsas</p>
<p><strong>Padrão </strong> : falso</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Restart</p></td>
<td align="left"><p>Suporta o adiamento do computador após a instalação do UE-V Agent.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>INSTALLFOLDER</p></td>
<td align="left"><p>Permite que uma pasta de instalação diferente seja definida para o UE-V Agent ou o UE-V Generator.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>MUENABLED</p></td>
<td align="left"><p>Permite que a instalação aceite a opção a ser incluída no programa Microsoft Update.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ACCEPTLICENSETERMS</p></td>
<td align="left"><p>Permite que o UE-V seja instalado silenciosamente. Isso deve ser definido como <strong> true </strong> para instalar o UE-V silenciosamente e ignorar a necessidade de que o usuário aceite os termos de licença do UE-v. Se definido como <strong> falso </strong> ou deixado vazio, o usuário recebe uma mensagem de erro e UE-V não está instalado.</p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Este parâmetro é necessário para instalar o UE-V silenciosamente.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Restart</p></td>
<td align="left"><p>Impede uma reinicialização obrigatória após a instalação do UE-V Agent.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Atualize o UE-V Agent

As atualizações para o software do agente do UE-V são fornecidas por meio do Microsoft Update. Você pode implantar as atualizações do UE-V Agent usando sistemas de infraestrutura ESD (Enterprise Software Distribution).

Durante uma atualização do UE-V Agent, o grupo padrão de modelos de localização de configurações para aplicativos e configurações do Windows comuns podem ser atualizados.

### Atualize o agente do UE-V 2. x

O agente UE-V 2. x introduz muitos recursos novos e modifica como e quando o agente carrega o conteúdo para o compartilhamento de armazenamento de configurações. O processo de atualização automatiza essas alterações. Para atualizar o UE-V Agent, execute o pacote de instalação do UE-V Agent (AgentSetup.exe, AgentSetupx86.msi ou AgentSetupx64.msi) nos computadores dos usuários.

**Observação**  
Ao atualizar o UE-V Agent, você deve usar o mesmo tipo de instalador (arquivo. exe ou pacote MSI) que instalou o UE-V Agent anterior. Por exemplo, use o AgentSetup.exe do UE-V 2 para atualizar os agentes do UE-V 1,0 que foram instalados usando o AgentSetup.exe.



As configurações a seguir são preservadas quando o programa de configuração do agente é executado:

-   Caminho de armazenamento de configurações

-   Configurações do registro

-   Tarefas agendadas (as configurações de intervalo são redefinidas para seus padrões)

**Observação**  
Um computador com os modelos de localização de configurações do UE-V 2. x que são registrados no UE-V 1,0 Agent registra erros no log de eventos do Windows.



Você pode usar o Gerenciador de configuração do Microsoft System Center 2012 ou outra ferramenta de distribuição de software corporativo para automatizar e distribuir a atualização do UE-V Agent.

**Recomendações:** Recomendamos que você atualize todos os agentes do UE-V 1,0 em um ambiente de computação, mas isso não é necessário. Os modelos de localização de configurações do UE-V 2. x podem interagir com um agente do UE-V 1,0, pois eles só compartilham as configurações do caminho de armazenamento de configurações. No entanto, recomendamos que você mova as implantações para uma única versão do agente para simplificar o gerenciamento e para dar suporte a UE-V.

### Reparar o UE-V Agent após uma atualização malsucedida

Você pode enfrentar erros após tentar uma das seguintes operações:

-   Atualização do UE-V 1,0 para o UE-V 2

-   Atualize para uma versão mais recente do Windows, por exemplo, do Windows 7 para o Windows 8 ou do Windows 8 para o Windows 8,1.

-   Desinstalar o agente após a atualização do UE-V Agent

Para resolver problemas, tente reparar o UE-V Agent inserindo esse comando em um prompt de comando no computador em que o agente está instalado.

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

Em seguida, você pode repetir o processo de desinstalação ou atualizar instalando a versão mais recente do UE-V Agent.






## Tópicos relacionados


[Preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









