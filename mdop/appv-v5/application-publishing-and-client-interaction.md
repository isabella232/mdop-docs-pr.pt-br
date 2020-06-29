---
title: Publicação de aplicativos e interação com clientes
description: Publicação de aplicativos e interação com clientes
author: dansimp
ms.assetid: c69a724a-85d1-4e2d-94a2-7ffe0b47d971
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b6080a501a8fdd2a39876ff979aa7a2982c76bbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796574"
---
# Publicação de aplicativos e interação com clientes


Este artigo fornece informações técnicas sobre operações comuns do cliente App-V e sua integração com o sistema operacional local.

-   [Arquivos de pacote App-V criados pelo sequenciador](#bkmk-appv-pkg-files-list)

-   [O que há no arquivo do AppV?](#bkmk-appv-file-contents)

-   [Locais do armazenamento de dados do cliente App-V](#bkmk-files-data-storage)

-   [Registro do pacote](#bkmk-pkg-registry)

-   [Comportamento da loja de pacotes do App-V](#bkmk-pkg-store-behavior)

-   [Registro e dados em roaming](#bkmk-roaming-reg-data)

-   [Gerenciamento do ciclo de vida do aplicativo cliente do App-V](#bkmk-clt-app-lifecycle)

-   [Integração de pacotes do App-V](#bkmk-integr-appv-pkgs)

-   [Processamento dinâmico de configuração](#bkmk-dynamic-config)

-   [Montagens lado a lado](#bkmk-sidebyside-assemblies)

-   [Registro em log do cliente](#bkmk-client-logging)

Para obter informações de referência adicionais, consulte a [página de download de recursos da documentação do Microsoft Application Virtualization (App-V)](https://www.microsoft.com/download/details.aspx?id=27760).

## <a href="" id="bkmk-appv-pkg-files-list"></a>Arquivos de pacote App-V criados pelo sequenciador


O sequenciador cria pacotes do App-V e produz um aplicativo virtualizado. O processo de sequenciamento cria os seguintes arquivos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Arquivo</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>. AppV</p></td>
<td align="left"><ul>
<li><p>O arquivo de pacote principal, que contém os ativos capturados e as informações de estado do processo de sequenciamento.</p></li>
<li><p>Arquitetura do arquivo de pacote, informações de publicação e registro em um formulário com token que pode ser reaplicado a um computador e a um usuário específico após a entrega.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>. MSI</p></td>
<td align="left"><p>Wrapper de implantação executável que você pode usar para implantar arquivos. AppV manualmente ou usando uma plataforma de implantação de terceiros.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>Arquivo usado para personalizar os parâmetros de publicação padrão para todos os aplicativos em um pacote que é implantado globalmente para todos os usuários em um computador que esteja executando o cliente App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>Arquivo usado para personalizar os parâmetros de publicação de todos os aplicativos em um pacote que é implantado para um usuário específico em um computador que esteja executando o cliente App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Resumo das mensagens resultantes do processo de sequenciamento, incluindo drivers omitidos, arquivos e locais do registro.</p></td>
</tr>
<tr class="even">
<td align="left"><p>. FICHEIRO</p></td>
<td align="left"><p><em>Opcional: </em> arquivo do acelerador de pacote usado para recriar automaticamente um pacote de aplicativo virtual sequenciado anteriormente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Opcional: </em> arquivo de modelo do sequenciador usado para manter as configurações do sequenciador reutilizadas comumente.</p></td>
</tr>
</tbody>
</table>

 

Para obter informações sobre o sequenciamento, consulte o [Guia de sequenciamento do Application Virtualization 5,0](https://www.microsoft.com/download/details.aspx?id=27760).

## <a href="" id="bkmk-appv-file-contents"></a>O que há no arquivo do AppV?


O arquivo do AppV é um contêiner que armazena arquivos XML e não XML juntos em uma única entidade. Esse arquivo é criado a partir do formato AppX, que se baseia no padrão Open Packaging Conventions (OPC).

Para exibir o conteúdo do arquivo do AppV, faça uma cópia do pacote e, em seguida, renomeie o arquivo copiado para uma extensão ZIP.

O arquivo do AppV contém a seguinte pasta e arquivos, que são usados ao criar e publicar um aplicativo virtual:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Root</p></td>
<td align="left"><p>Pasta de arquivos</p></td>
<td align="left"><p>Diretório que contém o sistema de arquivos para o aplicativo virtualizado que é capturado durante a sequenciagem.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types]. xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Lista dos principais tipos de conteúdo no arquivo do AppV (por exemplo, DLL, EXE, BIN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Layout do arquivo do AppV, que usa elementos File, Block e BlockMap que habilitam o local e a validação dos arquivos no pacote App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Metadados do pacote que contém as informações necessárias para adicionar, publicar e iniciar o pacote. Inclui pontos de extensão (associações de tipo de arquivo e atalhos) e os nomes e GUIDs associados ao pacote.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Lista de arquivos capturados durante o sequenciamento, incluindo atributos (por exemplo, diretórios, arquivos, pastas opacas, pastas vazias e nomes longos e curtos).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Informações sobre o computador de sequenciamento (versão do sistema operacional, versão do Internet Explorer, versão do .NET Framework) e processo (atualização, versão do pacote).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry. dat</p></td>
<td align="left"><p>Arquivo DAT</p></td>
<td align="left"><p>Chaves do registro e valores capturados durante o processo de sequenciamento do pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Lista de arquivos para o bloco de recursos Primary e Publishing. O bloco de recursos de publicação contém os arquivos ICO e partes de arquivos (EXE e DLL) necessárias para publicar o pacote. Quando presente, o bloco de recursos principal inclui arquivos que foram otimizados para streaming durante o processo de sequenciamento.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a>Locais do armazenamento de dados do cliente App-V


O cliente App-V executa tarefas para garantir que os aplicativos virtuais sejam executados corretamente e funcionem como aplicativos instalados localmente. O processo de abrir e executar aplicativos virtuais requer o mapeamento do sistema de arquivos virtual e do registro para garantir que o aplicativo tenha os componentes obrigatórios de um aplicativo tradicional esperado pelos usuários. Esta seção descreve os ativos necessários para executar aplicativos virtuais e lista o local onde o App-V armazena os ativos.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Localização</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Repositório de pacotes</p></td>
<td align="left"><p>%ProgramData%\App-V</p></td>
<td align="left"><p>Local padrão para arquivos de pacote somente leitura</p></td>
</tr>
<tr class="even">
<td align="left"><p>Catálogo da máquina</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contém documentos de configuração por máquina</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Catálogo de usuários</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contém documentos de configuração por usuário</p></td>
</tr>
<tr class="even">
<td align="left"><p>Backups de atalho</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Armazena os pontos de integração anteriores que habilitam a restauração em pacote cancelar publicação</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Roaming de cópia em gravação (vaca)</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Localização de roaming gravável para a modificação do pacote</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copiar em gravação (vaca) local</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Local não móvel gravável para a modificação do pacote</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registro do computador</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contém informações de estado do pacote, incluindo VReg para pacotes publicados de máquina ou globalmente (Hive da máquina)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registro de usuário</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contém informações de estado do pacote do usuário, incluindo VReg</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Classes de registro de usuário</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Contém informações adicionais do estado do pacote do usuário</p></td>
</tr>
</tbody>
</table>

 

Detalhes adicionais para a tabela são fornecidos na seção abaixo e em todo o documento.

### Repositório de pacotes

O cliente App-V gerencia os ativos de aplicativos montados no armazenamento de pacotes. Esse local de armazenamento padrão é `%ProgramData%\App-V` , mas você pode configurá-lo durante ou após a instalação usando o `Set-AppVClientConfiguration` comando do PowerShell, que modifica o registro local ( `PackageInstallationRoot` valor na `HKLM\Software\Microsoft\AppV\Client\Streaming` chave). O repositório de pacotes deve estar localizado em um caminho local no sistema operacional do cliente. Os pacotes individuais são armazenados no repositório de pacotes em subdiretórios nomeados para o GUID do pacote e o GUID da versão.

Exemplo de um caminho para um aplicativo específico:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Para alterar o local padrão do repositório de pacotes durante a instalação, consulte [como implantar o cliente App-V](how-to-deploy-the-app-v-client-gb18030.md).

### Repositório de conteúdo compartilhado

Se o cliente App-V estiver configurado no modo de repositório de conteúdo compartilhado, nenhum dado será gravado em disco quando ocorrer uma falha de fluxo, o que significa que os pacotes exigem espaço em disco local mínimo (dados de publicação). O uso de menos espaço em disco é altamente desejável em ambientes VDI, em que o armazenamento local pode ser limitado e o fluxo de aplicativos de um local de rede de alto desempenho (como uma SAN) é preferível. Para obter mais informações sobre o modo de repositório de conteúdo compartilhado, consulte <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Observação**  O repositório do computador e do pacote devem estar localizados em uma unidade local, mesmo quando você estiver usando configurações compartilhadas de repositório de conteúdo para o cliente App-V.

 

### Catálogos de pacotes

O cliente App-V gerencia os seguintes dois locais baseados em arquivos:

-   **Catálogos (usuário e computador).**

-   **Locais do registro** – depende de como o pacote é direcionado para publicação. Há um catálogo (armazenamento de dados) para o computador e um catálogo para cada usuário individual. O catálogo do computador armazena informações globais aplicáveis a todos os usuários ou qualquer usuário, e o catálogo do usuário armazena as informações aplicáveis a um usuário específico. O catálogo é um conjunto de configurações dinâmicas e arquivos de manifesto; Há dados discretos para o arquivo e o registro por versão do pacote. 

### Catálogo da máquina

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Armazena documentos do pacote que estão disponíveis para os usuários do computador, quando os pacotes são adicionados e publicados. No entanto, se um pacote for "global" no momento da publicação, as integrações estarão disponíveis para todos os usuários.</p>
<p>Se um pacote for não global, as integrações serão publicadas somente para usuários específicos, mas ainda há recursos globais modificados e visíveis para qualquer pessoa no computador cliente (por exemplo, o diretório do pacote está em um local de disco compartilhado).</p>
<p>Se um pacote estiver disponível para um usuário no computador (global ou não global), o manifesto será armazenado no catálogo da máquina. Quando um pacote é publicado globalmente, há um arquivo de configuração dinâmico, armazenado no catálogo da máquina; Portanto, a determinação de se um pacote é global é definida de acordo com a existência de um arquivo de política (arquivo UserDeploymentConfiguration) no catálogo da máquina.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Local de armazenamento padrão</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Este local não é o mesmo que o local de armazenamento do pacote. O repositório de pacotes é a cópia dourada ou pristine dos arquivos do pacote.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivos no catálogo do computador</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml (pacote publicado globalmente)</p></li>
<li><p>UserDeploymentConfiguration.xml (pacote publicado globalmente)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Localização adicional do catálogo do computador, usado quando o pacote faz parte de um grupo de conexões</p></td>
<td align="left"><p>O local a seguir é além do local do pacote específico mencionado acima:</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivos adicionais no catálogo do computador quando o pacote fizer parte de um grupo de conexões</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (grupo de conexão publicada globalmente)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### Catálogo de usuários

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Criado durante o processo de publicação. Contém informações usadas para publicar o pacote e também usado no lançamento para garantir que um pacote seja provisionado para um usuário específico. Criado em um local de roaming e inclui informações de publicação específicas do usuário.</p>
<p>Quando um pacote é publicado para um usuário, o arquivo de política é armazenado no catálogo do usuário. Ao mesmo tempo, uma cópia do manifesto também é armazenada no catálogo do usuário. Quando uma qualificação de pacote é removida para um usuário, os arquivos de pacote relevantes são removidos do catálogo de usuários. Olhando para o catálogo do usuário, um administrador pode visualizar a presença de um arquivo de configuração dinâmico, que indica que o pacote tem direito para esse usuário.</p>
<p>Para usuários de roaming, o catálogo do usuário precisa estar em um local de roaming ou compartilhado para preservar o comportamento herdado do App-V do direcionamento de usuários por padrão. A qualificação e a política são vinculadas a um usuário, não um computador, para que eles possam fazer roaming com o usuário quando forem provisionados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Local de armazenamento padrão</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivos no catálogo do usuário</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml ou UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Local de catálogo do usuário adicional, usado quando o pacote faz parte de um grupo de conexões</p></td>
<td align="left"><p>O local a seguir é além do local do pacote específico mencionado acima:</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivo adicional no catálogo do computador quando o pacote fizer parte de um grupo de conexões</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### Backups de atalho

Durante o processo de publicação, o cliente App-V faz o backup de todos os atalhos e pontos de integração para `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` esse backup permite que a restauração desses pontos de integração para as versões anteriores sejam canceladas quando o pacote é cancelado.

### Copiar em arquivos de gravação

O repositório de pacotes contém uma cópia pristine dos arquivos de pacote que foram retransmitidos do servidor de publicação. Durante a operação normal de um aplicativo App-V, o usuário ou serviço pode exigir alterações nos arquivos. Essas alterações não são feitas no repositório de pacotes para preservar a capacidade de reparar o aplicativo, o que remove essas alterações. Esses locais, chamados de cópia na gravação (vaca), dão suporte a locais de roaming e não móveis. O local onde as modificações são armazenadas depende de onde o aplicativo foi programado para escrever alterações em uma experiência nativa.

### VACA roaming

O local de roaming vaca descrito acima armazena alterações em arquivos e diretórios direcionados para o local típico% AppData% ou o local \\Users\\{username}\\AppData\\Roaming. Esses diretórios e arquivos são então movidos de acordo com as configurações do sistema operacional.

### Local vaca

O local vaca local é semelhante ao local de roaming, mas as pastas e os arquivos não são movidos para outros computadores, mesmo se o suporte a roaming tiver sido configurado. O local vaca local descrito acima armazena alterações aplicáveis a janelas típicas e não ao local% AppData%. As pastas listadas irão variar, mas haverá dois locais para qualquer local típico do Windows (por exemplo, AppData comuns e AppDatas comuns). O **S** significa o local restrito quando o serviço virtual solicita a alteração como um usuário elevado diferente dos usuários conectados. O local não-**S** armazena alterações baseadas em usuários.

## <a href="" id="bkmk-pkg-registry"></a>Registro do pacote


Antes de um aplicativo poder acessar os dados do registro do pacote, o cliente App-V deve disponibilizar os dados do registro do pacote para os aplicativos. O cliente App-V usa o registro real como um repositório de backup para todos os dados do registro.

Quando um novo pacote é adicionado ao cliente App-V, uma cópia do registro. O arquivo DAT do pacote é criado em `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . O nome do arquivo é o GUID da versão com a extensão. Extensão DAT. O motivo pelo qual essa cópia é feita é garantir que o arquivo de Hive real do pacote nunca seja usado, o que impediria a remoção do pacote posteriormente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry. dat do repositório de pacotes</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</strong></p></td>
</tr>
</tbody>
</table>

 

Quando o primeiro aplicativo do pacote é iniciado no cliente, o cliente prepara ou copia o conteúdo do arquivo hive, recriando os dados do registro do pacote em um local alternativo `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` . Os dados do registro em estágios têm dois tipos distintos de dados da máquina e dados do usuário. Os dados da máquina são compartilhados entre todos os usuários do computador. Os dados do usuário são testados para cada usuário em um local específico do usuário `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` . Os dados da máquina são removidos basicamente no momento da remoção do pacote e os dados do usuário são removidos em uma operação de cancelamento de usuário do usuário.

### Transferência do registro do pacote versus transferência do registro do grupo de conexão

Quando os grupos de conexão estão presentes, o processo anterior de preparação do registro é verdadeiro, mas em vez de ter um arquivo de Hive para processar, há mais de um. Os arquivos são processados na ordem em que aparecem no XML do grupo de conexão, com o primeiro autor vencedor de qualquer conflito.

O registro em estágios persiste da mesma maneira que no caso do único pacote. Os dados do registro do usuário em estágios permanecem para o grupo de conexão até que ele seja desativado; os dados do registro do computador em estágios são removidos na remoção do grupo de conexão.

### Registro virtual

A finalidade do registro virtual (VREG) é fornecer um único modo de exibição mesclado do registro do pacote e do registro nativo para aplicativos. Ele também fornece a funcionalidade Copy-on-Write (vaca), que é qualquer alteração feita no registro do contexto de um processo virtual é feita para um local vaca separado. Isso significa que o VREG deve combinar até três locais de registro separados em um único modo de exibição com base nos locais preenchidos do registro vaca- &gt; Package- &gt; Native. Quando for feita uma solicitação para os dados do registro, ele será localizado na ordem até encontrar os dados que ele estava solicitando. Ou seja, se houver um valor armazenado em um local do vaca, ele não vai para outros locais, no entanto, se não houver dados no local vaca, ele passará para o pacote e, em seguida, a localização nativa até encontrar os dados apropriados.

### Locais do registro

Há dois locais do registro do pacote e dois locais de grupo de conexão onde o cliente App-V armazena as informações do registro, dependendo se o pacote é publicado individualmente ou como parte de um grupo de conexão. Há três locais vaca para pacotes e três para grupos de conexão, que são criados e gerenciados pelo VREG. As configurações de pacotes e grupos de conexão não são compartilhadas:

**Pacote único de VReg:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Localização</strong></p></td>
<td align="left"><p><strong>Descrição</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>VACA</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\REGISTRY (processo de elevação do computador somente pode gravar)</p></li>
<li><p>Registry\Client\Packages\PkgGUID\REGISTRY do usuário (usuário móvel qualquer coisa escrita em HKCU, exceto Software\Classes</p></li>
<li><p>Classes\Client\Packages\PkgGUID\REGISTRY do registro do usuário (HKCU\Software\Classes de gravação e HKLM para processo não elevado)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Pacote</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry do registro do usuário</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>ISCSI</strong></p></td>
<td align="left"><ul>
<li><p>Local do registro do aplicativo nativo</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**VReg do grupo de conexão:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Localização</strong></p></td>
<td align="left"><p><strong>Descrição</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>VACA</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (processo de elevação do computador somente pode gravar)</p></li>
<li><p>Registry\Client\PackageGroups\GrpGUID\REGISTRY do usuário (qualquer coisa escrita para HKCU, exceto Software\Classes</p></li>
<li><p>Classes\Client\PackageGroups\GrpGUID\REGISTRY do registro do usuário</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Pacote</strong></p></td>
<td align="left"><ul>
<li><p>Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY do registro do usuário</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>ISCSI</strong></p></td>
<td align="left"><ul>
<li><p>Local do registro do aplicativo nativo</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Há dois locais do vaca para HKLM; processos elevados e não elevados. Processos elevados sempre gravam as alterações de HKLM no vaca seguro em HKLM. Processos não elevados sempre gravam as alterações de HKLM nas vaca não seguras em HKCU\\Software\\Classes. Quando um aplicativo lê alterações de HKLM, processos elevados lêem alterações do vaca seguro em HKLM. Leituras não elevadas de ambos, favorecendo as alterações feitas no vaca não seguro primeiro.

### Teclas de passagem

As teclas de passagem permitem que um administrador configure determinadas teclas para que elas só possam ser lidas do registro nativo, ignorando os locais do pacote e do vaca. Locais de passagem são globais para a máquina (não específico do pacote) e podem ser configurados adicionando o caminho à chave, que deve ser tratado como pass-through para o valor **reg \ _MULTI \ _SZ** chamado **PassThroughPaths** da chave `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` . Qualquer chave que aparece sob esse valor de cadeia de caracteres múltipla (e seus filhos) será tratada como pass-through.

Os locais a seguir são configurados como locais de passagem por padrão:

-   HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY \ _CURRENT \ _USER configurações \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies

-   HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies

A finalidade das teclas de passagem é garantir que um aplicativo virtual não grave dados do registro no VReg que é necessário para aplicativos não virtuais para operação ou integração bem-sucedida. A chave Policies garante que as configurações baseadas em políticas de grupo definidas pelo administrador sejam utilizadas e não por configurações de pacote. A chave AppModel é necessária para integração com aplicativos baseados na interface do usuário moderna do Windows. Recomendamos que a administração não modifique nenhuma das teclas de passagem padrão, mas em alguns casos, com base no comportamento do aplicativo, talvez seja necessário adicionar teclas de passagem adicionais.

## <a href="" id="bkmk-pkg-store-behavior"></a>Comportamento da loja de pacotes do App-V


O App-V 5 gerencia o repositório de pacotes, que é o local onde os arquivos de ativos expandidos do arquivo do AppV são armazenados. Por padrão, esse local está armazenado em%ProgramData%\\App-V e é limitado em termos de recursos de armazenamento apenas pelo espaço livre em disco. O repositório do pacote é organizado pelos GUIDs do pacote e da versão, conforme mencionado na seção anterior.

### Adicionar pacotes

Os pacotes do App-V são testados após a adição ao computador com o cliente App-V. O cliente App-V fornece transferência sob demanda. Durante a publicação ou um Add-AppVClientPackage manual, a estrutura de dados é criada no repositório de pacotes (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}). Os arquivos de pacote identificados no bloco de publicação definido no StreamMap.xml são adicionados ao sistema e as pastas de nível superior e os arquivos filho testados para garantir que os ativos de aplicativo apropriados existam na inicialização.

### Montando pacotes

Os pacotes podem ser carregados explicitamente usando o PowerShell `Mount-AppVClientPackage` ou usando a **interface do usuário do cliente App-V** para baixar um pacote. Esta operação carrega completamente o pacote inteiro no repositório de pacotes.

### Pacotes de streaming

O cliente App-V pode ser configurado para alterar o comportamento padrão do streaming. Todas as políticas de streaming são armazenadas na seguinte chave do `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` registro: As políticas são definidas usando o cmdlet do PowerShell `Set-AppvClientConfiguration` . As políticas a seguir se aplicam ao streaming:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Política</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>No Windows 8 permite o streaming em redes 3G e celulares</p></td>
</tr>
<tr class="even">
<td align="left"><p>Carregar</p></td>
<td align="left"><p>Especifica a configuração de carga em segundo plano:</p>
<p><strong>0 </strong> - desativado</p>
<p><strong>1 </strong> – pacotes usados anteriormente</p>
<p><strong>2 </strong> – todos os pacotes</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>A pasta raiz do repositório de pacotes no computador local</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>A raiz substitui a do qual os pacotes devem ser transmitidos</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Habilita o uso de repositório de conteúdo compartilhado para cenários de VDI</p></td>
</tr>
</tbody>
</table>

 

 

Essas configurações afetam o comportamento dos ativos do pacote do App-V de streaming para o cliente. Por padrão, o App-V só baixa os ativos necessários após o download da publicação inicial e dos blocos de recursos primários. Há três comportamentos específicos em relação aos pacotes de streaming que devem ser explicados:

-   Streaming em segundo plano

-   Streaming otimizado

-   Falhas de fluxo

### Streaming em segundo plano

O cmdlet do PowerShell `Get-AppvClientConfiguration` pode ser usado para determinar o modo atual para streaming em segundo plano com a configuração AutoLoad e modificada com o cmdlet Set-AppvClientConfiguration ou a partir do registro (chave HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming). Streaming em segundo plano é uma configuração padrão em que a configuração de AutoLoad está definida para baixar pacotes usados anteriormente. O comportamento com base na configuração padrão (valor = 1) baixa os blocos de dados do App-V em segundo plano após a inicialização do aplicativo. Essa configuração pode ser desabilitada juntos (valor = 0) ou habilitado para todos os pacotes (valor = 2), se foram iniciados.

### Streaming otimizado

Os pacotes do App-V podem ser configurados com um bloco de recursos principal durante o sequenciamento. Essa configuração permite que o engenheiro de sequenciamento monitore arquivos de inicialização para um aplicativo específico, ou aplicativos, e marque os blocos de dados no pacote App-V para streaming na primeira inicialização de qualquer aplicativo no pacote.

### Falhas de fluxo

Após o fluxo inicial de todos os dados de publicação e o bloco de recursos principal, as solicitações de arquivos adicionais executam falhas de fluxo. Esses blocos de dados são baixados para o repositório de pacotes conforme o necessário. Isso permite que um usuário Baixe apenas uma pequena parte do pacote, geralmente suficiente para iniciar o pacote e executar tarefas normais. Todos os outros blocos são baixados quando um usuário inicia uma operação que requer dados que não estão no repositório de pacotes.

Para obter mais informações sobre o compartilhamento de pacotes do App-V, acesse: <https://go.microsoft.com/fwlink/?LinkId=392770> .

O sequenciamento para otimização de transmissão está disponível em: <https://go.microsoft.com/fwlink/?LinkId=392771> .

### Atualizações de pacote

Os pacotes do App-V exigem atualização ao longo do ciclo de vida do aplicativo. As atualizações do pacote do App-V são semelhantes à operação de publicação do pacote, pois cada versão será criada em seu próprio local PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . A operação de atualização é otimizada pela criação de links rígidos para arquivos idênticos e transmitidos de outras versões do mesmo pacote.

### Remoção de pacote

O comportamento do cliente App-V quando os pacotes são removidos depende do método usado para remoção. Usando uma infraestrutura completa do App-V para cancelar a publicação do aplicativo, os arquivos de catálogo do usuário (catálogo de computadores para aplicativos publicados globalmente) são removidos, mas retém o local do repositório de pacotes e locais do vaca. Quando o cmdlet do PowerShell `Remove-AppVClientPackge` é usado para remover um pacote do App-V, o local do repositório de pacotes é limpo. Lembre-se de que cancelar a publicação de um pacote do App-V a partir do servidor de gerenciamento não executa uma operação de remoção. Nenhuma operação removerá os arquivos de pacote do pacote de armazenamento.

## <a href="" id="bkmk-roaming-reg-data"></a>Registro e dados em roaming


O App-V 5 pode oferecer uma experiência quase nativa ao fazer roaming, dependendo de como o aplicativo sendo usado é gravado. Por padrão, o App-V roams AppData que está armazenado no local de roaming, com base na configuração de roaming do sistema operacional. Outros locais para armazenamento de dados baseados em arquivos não fazem roaming de um computador para outro, já que eles estão em locais que não estão em roaming.

### <a href="" id="bkmk-clt-inter-roam-reqs"></a>Requisitos de roaming e armazenamento de dados de catálogo do usuário

O App-V armazena dados, que representam o estado do catálogo do usuário, na forma de:

-   Arquivos em%appdata%\\Microsoft\\AppV\\Client\\Catalog

-   Configurações do registro em `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

Juntos, esses arquivos e configurações do registro representam o catálogo do usuário, portanto ambos devem ser movidos ou não devem ser movidos para um determinado usuário. O App-V não oferece suporte a roaming% AppData%, mas não ao roaming do perfil do usuário (registro) ou vice-versa.

**Observação**  O cmdlet **Repair-AppvClientPackage** não repara o estado de publicação de pacotes, onde o estado App-V do usuário em `HKEY_CURRENT_USER` está ausente ou incompatível com os dados em% AppData%.

 

### Dados baseados no registro

O roaming do registro do App-V se encaixa em dois cenários, conforme mostrado na tabela a seguir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenário</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicativos que são executados como usuários padrão</p></td>
<td align="left"><p>Quando um usuário padrão inicia um aplicativo App-V, os aplicativos HKLM e HKCU para aplicativos App-V são armazenados no hive HKCU do computador. Isso apresenta os dois caminhos distintos:</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {userid} \ SOFTWARE</p></li>
</ul>
<p>Os locais são habilitados para roaming com base nas configurações do sistema operacional.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicativos executados com elevação</p></td>
<td align="left"><p>Quando um aplicativo é iniciado com elevação:</p>
<ul>
<li><p>Os dados HKLM são armazenados no hive HKLM no computador local</p></li>
<li><p>Dados HKCU são armazenados no local do registro do usuário</p></li>
</ul>
<p>Nesse cenário, essas configurações não estão em roaming com configurações de roaming normal do sistema operacional, e os valores e as chaves do registro resultantes são armazenados no seguinte local:</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {userid} \ REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {Usuáriosid} \ SOFTWARE</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### App-V e redirecionamento de pastas

O App-V 5.0 SP2 dá suporte ao redirecionamento de pastas da pasta Roaming AppData (% AppData%). Quando o ambiente virtual é iniciado, o estado roaming de AppData do diretório roaming do usuário é copiado para o cache local. Por outro lado, quando o ambiente virtual é desligado, o cache local que está associado a um usuário específico do roaming de um usuário é transferido para o local real do diretório de AppData do roaming do usuário.

Um pacote típico tem vários locais mapeados no repositório de backup do usuário para configurações em AppData\\Local e AppData\\Roaming. Esses locais são a cópia em locais de gravação que são armazenados por usuário no perfil do usuário, e que são usados para armazenar alterações feitas nos diretórios do pacote do VFS e para proteger o pacote VFS padrão.

A tabela a seguir mostra locais locais e de roaming, quando o redirecionamento de pastas não foi implementado.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Diretório VFS no pacote</th>
<th align="left">Local mapeado do repositório de backup</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID de &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID de &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; \Windows do GUID &gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; forte &gt; </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID de &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

A tabela a seguir mostra locais locais e de roaming, quando o redirecionamento de pastas foi implementado para% AppData% e o local foi redirecionado (geralmente para um local de rede).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Diretório VFS no pacote</th>
<th align="left">Local mapeado do repositório de backup</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID de &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID de &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; \Windows do GUID &gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; \Microsoft\AppV\Client\VFS de alta segurança, &gt; </strong> &amp; lt; GUID &gt; \ appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID de &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

O driver VFS do cliente App-V atual não pode gravar em locais de rede, portanto, o cliente App-V detecta a presença do redirecionamento de pasta e copia os dados na unidade local durante a publicação e quando o ambiente virtual é iniciado. Depois que o usuário fechar o aplicativo App-V e o cliente App-V fechar o ambiente virtual, o armazenamento local do VFS AppData será copiado novamente para a rede, permitindo o roaming para outras máquinas, onde o processo será repetido. As etapas detalhadas dos processos são:

1.  Durante a publicação ou a inicialização do ambiente virtual, o cliente App-V detecta a localização do diretório AppData.

2.  Se o caminho de AppData do roaming for local ou ino local AppData\\Roaming for mapeado, nada acontecerá.

3.  Se o caminho de AppData do roaming não for local, o diretório VFS AppData será mapeado para o diretório local AppData.

Esse processo resolve o problema de um% AppData% não local que não é suportado pelo driver VFS do cliente App-V. No entanto, os dados armazenados nesse novo local não são movidos com o redirecionamento de pastas. Todas as alterações durante a execução do aplicativo acontecem para o local AppData local e devem ser copiadas para o local redirecionado. As etapas detalhadas desse processo são:

1.  Aplicativo App-V está desligado, o que desliga o ambiente virtual.

2.  O cache local do local de AppData do roaming é compactado e armazenado em um arquivo ZIP.

3.  Um carimbo de data/hora no final do processo de empacotamento ZIP é usado para nomear o arquivo.

4.  O carimbo de data/hora é registrado no registro: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime como o último carimbo de data/hora conhecido do AppData.

5.  O processo de redirecionamento de pastas é chamado para avaliar e iniciar o arquivo ZIP carregado no diretório roaming AppData.

O carimbo de data/hora é usado para determinar um cenário "último gravador WINS" se houver um conflito e usado para otimizar o download dos dados quando o aplicativo App-V for publicado ou o ambiente virtual for iniciado. O redirecionamento de pastas disponibilizará os dados de qualquer outro cliente coberto pela política de suporte e iniciará o processo de armazenamento dos dados do AppData\\Roaming no local AppData local no cliente. Os processos detalhados são:

1.  O usuário inicia o ambiente virtual iniciando um aplicativo.

2.  O ambiente virtual do aplicativo verifica o arquivo ZIP com carimbo de data/hora mais recente, se houver.

3.  O registro é verificado para o último carimbo de data/hora carregado conhecido, se houver.

4.  O arquivo ZIP mais recente é baixado, a menos que o último carimbo de data/hora de carregamento conhecido seja maior ou igual ao carimbo de data/hora do arquivo ZIP.

5.  Se o último carimbo de data/hora de carregamento conhecido local for anterior ao do arquivo ZIP mais recente no local roaming AppData, o arquivo ZIP será extraído para o diretório Temp local no perfil do usuário.

6.  Depois que o arquivo ZIP é extraído com êxito, o cache local do diretório roaming AppData é renomeado e os novos dados são movidos para o lugar.

7.  O diretório renomeado é excluído e o aplicativo é aberto com os dados de roaming salvos mais recentemente salvos.

Isso conclui o roaming bem-sucedido das configurações do aplicativo que estão presentes nos locais do AppData\\Roaming. A única outra condição que deve ser abordada é uma operação de reparo do pacote. Os detalhes do processo são:

1.  Durante o reparo, detecte se o caminho do diretório de AppData do roaming do usuário não é local.

2.  Mapear os destinos de caminho do roaming de AppData não locais são recriados os locais esperados de sites de mesmo roaming e locais.

3.  Exclua o carimbo de data/hora armazenado no registro, se houver.

Esse processo recriará os locais locais e de rede para AppData e removerá o registro do registro do carimbo de data/hora.

## <a href="" id="bkmk-clt-app-lifecycle"></a>Gerenciamento do ciclo de vida do aplicativo cliente do App-V


Em uma infraestrutura completa do App-V, após os aplicativos serem sequenciados, eles são gerenciados e publicados em usuários ou computadores por meio dos servidores de gerenciamento e publicação do App-V. Esta seção detalha as operações que ocorrem durante as operações do ciclo de vida do aplicativo comum do App-V (adicionar, publicar, iniciar, atualizar e remover) e os locais de arquivo e registro que são alterados e modificados da perspectiva do cliente App-V. As operações do cliente App-V são executadas como uma série de comandos do PowerShell iniciada no computador executando o cliente App-V.

Este documento enfoca as soluções de infraestrutura completa do App-V. Para obter informações específicas sobre a integração do App-V com o Configuration Manager 2012, acesse: <https://go.microsoft.com/fwlink/?LinkId=392773> .

As tarefas do ciclo de vida do aplicativo App-V são disparadas no logon do usuário (padrão), na inicialização da máquina ou nas operações com tempo de tela de fundo. As configurações para as operações do cliente App-V, incluindo servidores de publicação, intervalos de atualização, habilitação de script de pacote e outros, são configuradas durante a configuração do cliente ou pós-instalação com comandos do PowerShell. Consulte a seção como implantar o cliente no TechNet em: [como implantar o cliente App-V](how-to-deploy-the-app-v-client-gb18030.md) ou usar o PowerShell:

```powershell
get-command *appv*
```

### Atualização de publicação

O processo de atualização de publicação é composto por várias operações menores que são executadas no cliente App-V. Como o App-V é uma tecnologia de virtualização de aplicativos e não uma tecnologia de agendamento de tarefas, o Agendador de tarefas do Windows é usado para habilitar o processo no logon do usuário, na inicialização da máquina e em intervalos agendados. A configuração do cliente durante a configuração listada acima é o método preferencial ao distribuir o cliente para um grupo grande de computadores com as configurações corretas. Essas configurações de cliente podem ser configuradas com os seguintes cmdlets do PowerShell:

-   **Add-AppVPublishingServer:** Configura o cliente com um servidor de publicação App-V que fornece pacotes do App-V.

-   **Set-AppVPublishingServer:** Modifica as configurações atuais para o servidor de publicação App-V.

-   **Set-AppVClientConfiguration:** Modifica as configurações atuais para o cliente App-V.

-   **Sync-AppVPublishingServer:** Inicia um processo de atualização de publicação do App-V manualmente. Isso também é usado nas tarefas agendadas criadas durante a configuração do servidor de publicação.

O foco das seções a seguir é detalhando as operações que ocorrem durante diferentes fases de uma atualização de publicação do App-V. Os tópicos incluem:

-   Adicionando um pacote do App-V

-   Publicando um pacote do App-V

### Adicionando um pacote do App-V

Adicionar um pacote do App-V ao cliente é a primeira etapa do processo de atualização da publicação. O resultado final é o mesmo que o `Add-AppVClientPackage` cmdlet no PowerShell, exceto durante o processo de adição de atualização de publicação, o servidor de publicação configurado é contatado e passa uma lista de alto nível de aplicativos de volta para o cliente para obter informações mais detalhadas e não um único pacote Adicionar operação. O processo continua Configurando adições ou atualizações do cliente para pacote ou grupo de conexão e, em seguida, acessa o arquivo do AppV. Em seguida, o conteúdo do arquivo do AppV é expandido e colocado no sistema operacional local nos locais apropriados. Veja a seguir um fluxo de trabalho detalhado do processo, presumindo que o pacote esteja configurado para streaming de falhas.

**Como adicionar um pacote do App-V**

1.  Início manual via PowerShell ou início de sequência de tarefas do processo de atualização de publicação.

    1.  O cliente App-V faz uma conexão HTTP e solicita uma lista de aplicativos com base no destino. O processo de atualização de publicação dá suporte a máquinas ou usuários de destino.

    2.  O servidor de publicação App-V usa a identidade do destino de inicialização, usuário ou computador e consulta o banco de dados para obter uma lista de aplicativos qualificados. A lista de aplicativos é fornecida como uma resposta XML, que o cliente usa para enviar solicitações adicionais ao servidor para obter mais informações com base em cada pacote.

2.  O agente de publicação no cliente App-V executa todas as ações abaixo de serializadas.

    Avalie todos os grupos de conexão que são cancelados ou desativados, pois as atualizações de versão de pacote que fazem parte do grupo de conexão não podem ser processadas.

3.  Configure os pacotes identificando as operações de adição ou atualização.

    1.  O cliente App-V usa a API AppX do Windows e acessa o arquivo do AppV a partir do servidor de publicação.

    2.  O arquivo de pacote é aberto e o AppXManifest.xml e os StreamMap.xml são baixados para o armazenamento de pacotes.

    3.  Dados de bloco de publicação de fluxo completamente definidos no StreamMap.xml. Armazena os dados do bloco de publicação no pacote Store\\PkgGUID\\VerGUID\\Root.

        -   Ícones: destinos de pontos de extensão.

        -   Cabeçalhos executáveis portáteis (cabeçalhos PE): alvos de pontos de extensão que contêm as informações básicas sobre a imagem necessária em disco, acessados diretamente ou por meio de tipos de arquivo.

        -   Scripts: baixar o diretório de scripts para uso em todo o processo de publicação.

    4.  Preencha o repositório de pacotes:

        1.  Crie arquivos esparsos em disco que representem o pacote extraído para qualquer diretório listado.

        2.  Estágio arquivos e diretórios de nível superior em root.

        3.  Todos os outros arquivos são criados quando o diretório é listado como esparso em disco e em fluxo por demanda.

    5.  Criar as entradas do catálogo da máquina. Crie o Manifest.xml e DeploymentConfiguration.xml a partir dos arquivos de pacote (se nenhum arquivo de DeploymentConfiguration.xml no pacote tiver sido criado um espaço reservado).

    6.  Criar local do repositório de pacotes no registro HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog

    7.  Crie o arquivo Registry. dat do pacote de armazenamento para%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat

    8.  Registrar o pacote com o driver do modo kernel do App-V HKLM\\Microsoft\\Software\\AppV\\MAV

    9.  Invoque o script do arquivo AppxManifest.xml ou DeploymentConfig.xml para adicionar intervalo ao pacote.

4.  Configurar grupos de conexão adicionando e habilitando ou desabilitando.

5.  Remover objetos que não são publicados no destino (usuário ou computador).

    **Observação**  Isso não executará uma exclusão de pacote, mas, em vez disso, removerá pontos de integração para o destino específico (usuário ou computador) e removerá arquivos de catálogo do usuário (arquivos de catálogo do computador para publicação global).

     

6.  Invocar a montagem da carga em segundo plano com base na configuração do cliente.

7.  Os pacotes que já têm informações de publicação para a máquina ou usuário são restaurados imediatamente.

    **Observação**  Essa condição ocorre como um produto de remoção sem cancelar a publicação com a adição de plano de fundo do pacote.

     

Isso conclui um pacote App-V Add do processo de atualização de publicação. A próxima etapa é publicar o pacote para o destino específico (computador ou usuário).

![pacote adicionar dados de arquivo e registro](images/packageaddfileandregistrydata.png)

### Publicando um pacote do App-V

Durante a operação de atualização de publicação, a operação de publicação específica (Publish-AppVClientPackage) adiciona entradas ao catálogo do usuário, mapeia a qualificação ao usuário, identifica o repositório local e termina ao completar qualquer etapa de integração. Veja a seguir as etapas detalhadas.

**Como publicar e o pacote do App-V**

1.  Entradas de pacote são adicionadas ao catálogo de usuários

    1.  Pacotes direcionados pelo usuário: o UserDeploymentConfiguration.xml e os UserManifest.xml são colocados na máquina no catálogo do usuário

    2.  Pacotes direcionados por máquina (global): o UserDeploymentConfiguration.xml é colocado no catálogo do computador

2.  Registre o pacote com o driver de modo kernel para o usuário em HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Executar tarefas de integração.

    1.  Criar pontos de extensão.

    2.  Armazene informações de backup no registro do usuário e perfil móvel (backups de atalho).

        **Observação**  Isso permite que os pontos de extensão da restauração se o pacote seja cancelado.

         

    3.  Executar scripts destinados para a publicação do tempo.

Publicar um pacote do App-V que faz parte de um grupo de conexão é muito semelhante ao processo acima. Para grupos de conexão, o caminho que armazena as informações específicas do catálogo inclui PackageGroups como um filho do diretório de catálogo. Examine as informações de catálogo do computador e dos usuários acima para obter detalhes.

![pacote adicionar dados de arquivo e registro-global](images/packageaddfileandregistrydata-global.png)

### Início do aplicativo

Após o processo de atualização de publicação, o usuário é iniciado e reinicia subseqüentemente um aplicativo App-V. O processo é muito simples e otimizado para iniciar rapidamente com um mínimo de tráfego de rede. O cliente App-V verifica o caminho para o catálogo do usuário em busca de arquivos criados durante a publicação. Depois que os direitos para iniciar o pacote são estabelecidos, o cliente App-V cria um ambiente virtual, começa a transmitir os dados necessários e aplica os arquivos de manifesto e de configuração de implantação apropriados durante a criação do ambiente virtual. Com o ambiente virtual criado e configurado para o pacote e o aplicativo específico, o aplicativo é iniciado.

**Como iniciar aplicativos App-V**

1.  O usuário inicia o aplicativo clicando em um atalho ou em uma chamada de tipo de arquivo.

2.  O cliente App-V Verifica a existência no catálogo do usuário para os seguintes arquivos

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  Se os arquivos estiverem presentes, o aplicativo será qualificado para esse usuário específico, e o aplicativo iniciará o processo de inicialização. Não há tráfego de rede neste ponto.

4.  Em seguida, o cliente App-V Verifica se o caminho do pacote registrado para o serviço do cliente App-V está localizado no registro.

5.  Ao encontrar o caminho para o repositório de pacotes, o ambiente virtual é criado. Se esta for a primeira inicialização, o bloco de recursos principal será baixado, se houver.

6.  Após o download, o serviço App-V cliente consome os arquivos de manifesto e de configuração de implantação para configurar o ambiente virtual e todos os subsistemas do App-V são carregados.

7.  O aplicativo é iniciado. Para todos os arquivos ausentes no repositório de pacotes (arquivos esparsos), o App-V transmitirá falhas nos arquivos de acordo com a necessidade.

    ![pacote Adicionar arquivo e dados do registro-Stream](images/packageaddfileandregistrydata-stream.png)

### Atualizando um pacote do App-V

O processo de atualização do pacote do App-V 5 é diferente das versões mais antigas do App-V. O App-V oferece suporte a várias versões do mesmo pacote em um computador qualificado para usuários diferentes. Versões de pacote podem ser adicionadas a qualquer momento, pois o repositório de pacotes e os catálogos são atualizados com os novos recursos. O único processo específico para a adição de novos recursos de versão é a otimização do armazenamento. Durante uma atualização, somente os novos arquivos são adicionados ao novo local de armazenamento de versão, e os links físicos são criados para arquivos inalterados. Isso reduz o armazenamento geral apenas apresentando o arquivo em um local de disco e projeta-o em todas as pastas com uma entrada de local de arquivo no disco. Os detalhes específicos da atualização de um pacote do App-V são os seguintes:

**Como atualizar um pacote do App-V**

1.  O cliente App-V executa uma atualização de publicação e descobre uma versão mais recente de um pacote do App-V.

2.  Entradas de pacote são adicionadas ao catálogo apropriado para a nova versão

    1.  Pacotes direcionados pelo usuário: o UserDeploymentConfiguration.xml e os UserManifest.xml são colocados na máquina no catálogo do usuário em appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

    2.  Pacotes direcionados pelo computador (global): o UserDeploymentConfiguration.xml é colocado no catálogo do computador em%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

3.  Registre o pacote com o driver de modo kernel para o usuário em HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Executar tarefas de integração.

    -   Integre os pontos de extensão (EP) a partir dos arquivos de manifesto e de configuração dinâmica.

    1.  Os dados do EP baseados em arquivos são armazenados na pasta AppData usando pontos de junção do armazenamento de pacotes.

    2.  A versão 1 EPs já existe quando uma nova versão se torna disponível.

    3.  Os pontos de extensão são alternados para o local da versão 2 no computador ou catálogos do usuário para qualquer ponto de extensão mais recente ou atualizado.

5.  Executar scripts destinados para a publicação do tempo.

6.  Instale montagens lado a lado conforme necessário.

### Atualizando um pacote App-V em uso

A **partir do App-V 5 SP2**: se você tentar atualizar um pacote que está sendo usado por um usuário final, a tarefa de atualização será colocada em um estado pendente. A atualização será executada mais tarde, de acordo com as seguintes regras:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de tarefa</th>
<th align="left">Regra aplicável</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tarefa baseada em usuário, por exemplo, publicar um pacote para um usuário</p></td>
<td align="left"><p>A tarefa pendente será executada após o usuário fazer logoff e, em seguida, fazer logon novamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tarefa com base global, por exemplo, habilitar um grupo de conexão globalmente</p></td>
<td align="left"><p>A tarefa pendente será executada quando o computador for desligado e reiniciado.</p></td>
</tr>
</tbody>
</table>

 

Quando uma tarefa é colocada em um estado pendente, o cliente App-V também gera uma chave do registro para a tarefa pendente, da seguinte maneira:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa baseada em usuário ou globalmente</th>
<th align="left">Onde a chave do registro é gerada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tarefas baseadas em usuário</p></td>
<td align="left"><p>KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tarefas com base global</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

As seguintes operações devem ser concluídas para que os usuários possam usar a versão mais recente do pacote:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Adicionar o pacote ao computador</p></td>
<td align="left"><p>Esta tarefa é específica do computador e você pode executá-la a qualquer momento, completando as etapas na seção Adicionar pacote acima.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publicar o pacote</p></td>
<td align="left"><p>Consulte a seção publicação do pacote acima para ver as etapas. Esse processo requer que você atualize os pontos de extensão no sistema. Os usuários finais não podem usar o aplicativo quando você concluir essa tarefa.</p></td>
</tr>
</tbody>
</table>

 

Use os cenários de exemplo a seguir como um guia para a atualização de pacotes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenário</th>
<th align="left">Requisitos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>O pacote do App-V não está em uso quando você tenta atualizar</p></td>
<td align="left"><p>Nenhum dos seguintes componentes do pacote pode estar em uso: aplicativo virtual, servidor COM ou extensões Shell.</p>
<p>O administrador publica uma versão mais recente do pacote e a atualização funciona da próxima vez que um componente ou aplicativo dentro do pacote for iniciado. A nova versão do pacote é transmitida e executada. Nada mudou nesse cenário no App-V 5 SP2 de versões anteriores do App-V 5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>O pacote do App-V está em uso quando o administrador publica uma versão mais recente do pacote</p></td>
<td align="left"><p>A operação de atualização é definida como pendente pelo cliente App-V, o que significa que ele é enfileirado e executado mais tarde quando o pacote não está em uso.</p>
<p>Se o aplicativo do pacote estiver em uso, o usuário desliga o aplicativo virtual, após o qual a atualização pode ocorrer.</p>
<p>Se o pacote tiver extensões Shell (Office 2013), que são carregadas permanentemente pelo Windows Explorer, o usuário não pode estar conectado. Os usuários devem fazer logoff e fazer logon novamente para iniciar a atualização do pacote App-V.</p></td>
</tr>
</tbody>
</table>

 

### Publicação global versus usuário

Os pacotes do App-V podem ser publicados de uma das duas maneiras: Usuário que entitula um pacote App-V para um usuário ou grupo de usuários específico que entitula o pacote App-V para o computador inteiro para todos os usuários do computador. Uma vez que a atualização do pacote está pendente, e o pacote do App-V não está em uso, considere os dois tipos de publicação:

-   **Publicado globalmente**: o aplicativo é publicado em um computador; todos os usuários desse computador podem usá-lo. A atualização ocorrerá quando o serviço do cliente App-V for iniciado, o que significa efetivamente uma reinicialização do computador.

-   **Usuário publicado**: o aplicativo é publicado para um usuário. Se houver vários usuários na máquina, o aplicativo poderá ser publicado em um subconjunto de usuários. A atualização ocorrerá quando o usuário fizer logon ou quando for publicada novamente (periodicamente, atualização e avaliação de política do ConfigMgr, ou uma publicação/atualização periódica do App-V, ou explicitamente via comandos do PowerShell).

### Como remover um pacote do App-V

Remover aplicativos do App-V em uma infraestrutura completa é uma operação de cancelamento de publicação e não executa uma remoção de pacote. O processo é o mesmo que o processo de publicação acima, mas em vez de adicionar o processo de remoção reverte as alterações que foram feitas para pacotes do App-V.

### Reparando um pacote do App-V

A operação de reparo é muito simples, mas pode afetar muitos locais na máquina. Os locais de cópia em gravação (vaca) mencionados anteriormente são removidos e os pontos de extensão são desintegrados e, em seguida, integrados novamente. Revise os locais de posicionamento de dados do vaca revisando o local onde estão registrados no registro. Esta operação é feita automaticamente e não há controle administrativo além de iniciar uma operação de reparo no console do cliente App-V ou via PowerShell (Repair-AppVClientPackage).

## <a href="" id="bkmk-integr-appv-pkgs"></a>Integração de pacotes do App-V


A arquitetura do cliente App-V e do pacote fornece integração específica com o sistema operacional local durante a adição e a publicação de pacotes. Três arquivos definem os pontos de integração ou de extensão para um pacote do App-V:

-   AppXManifest.xml: armazenados dentro do pacote com cópias de fallback armazenadas no repositório de pacotes e no perfil do usuário. Contém as opções criadas durante o processo de sequenciamento.

-   DeploymentConfig.xml: fornece informações de configuração de pontos de extensão de integração com base em computador e usuário.

-   UserConfig.xml: um subconjunto do Deploymentconfig.xml que fornece apenas configurações baseadas em usuário e direciona somente pontos de extensão baseados em usuários.

### Regras de integração

Quando os aplicativos do App-V são publicados em um computador com o cliente App-V, algumas ações específicas são feitas conforme descrito na lista abaixo:

-   Publicação global: os atalhos são armazenados no local do perfil todos os usuários e outros pontos de extensão são armazenados no registro no hive HKLM.

-   Publicação do usuário: os atalhos são armazenados no perfil atual da conta do usuário e outros pontos de extensão são armazenados no registro no hive HKCU.

-   Backup e restauração: os dados de aplicativos nativos existentes e o registro (como registros FTA) são incluídos durante a publicação.

    1.  Os pacotes do App-V recebem Propriedade com base no último pacote integrado em que a propriedade é passada para o aplicativo App-V publicado mais recente.

    2.  As transferências de propriedade de um pacote App-V para outro quando o pacote App-V proprietário é cancelado. Isso não irá iniciar uma restauração dos dados ou do registro.

    3.  Restaure os dados de backup quando o último pacote for cancelado ou removido por cada ponto de extensão.

### Pontos de extensão

Os arquivos de publicação do App-V (manifesto e configuração dinâmica) fornecem vários pontos de extensão que permitem que o aplicativo se integre com o sistema operacional local. Esses pontos de extensão executam tarefas típicas de instalação do aplicativo, como o posicionamento de atalhos, a criação de associações de tipo de arquivo e o registro de componentes. Como esses são aplicativos virtualizados que não são instalados da mesma maneira em um aplicativo tradicional, há algumas diferenças. Veja a seguir uma lista de pontos de extensão abordados nesta seção:

-   Teclado

-   Associações de tipo de arquivo

-   Extensões do Shell

-   COM

-   Clientes de software

-   Funcionalidades do aplicativo

-   Manipulador de protocolo de URL

-   AppPath

-   Aplicativo virtual

### Teclado

O corte curto é um dos elementos básicos da integração com o sistema operacional e é a interface para a inicialização direta do usuário de um aplicativo App-V. Durante a publicação e a publicação de aplicativos App-V.

No manifesto do pacote e nos arquivos XML de configuração dinâmica, o caminho para um executável do aplicativo específico pode ser encontrado em uma seção semelhante à seguinte:

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

Conforme mencionado anteriormente, os atalhos do App-V são colocados por padrão no perfil do usuário com base na operação de atualização. Atualização global locais os atalhos no perfil todos os usuários e na atualização do usuário os armazena no perfil do usuário específico. O executável real é armazenado no repositório de pacotes. O local do arquivo ICO é um local com token no pacote App-V.

### Associações de tipo de arquivo

O cliente App-V gerencia as associações de tipo de arquivo do sistema operacional local durante a publicação, o que permite que os usuários usem invocações de tipo de arquivo ou abram um arquivo com uma extensão especialmente registrada (. docx) para iniciar um aplicativo App-V. As associações de tipo de arquivo estão presentes nos arquivos de configuração dinâmica e manifesto, conforme representado no exemplo abaixo:

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

**Observação**  Neste exemplo:

-   `<Name>.xdp</Name>` é a extensão

-   `<Name>AcroExch.XDPDoc</Name>` é o valor ProgId (que aponta para o ProgId adjacente)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` é a linha de comando, que aponta para o executável do aplicativo

 

### Extensões de shell

Extensões do shell são incorporadas ao pacote automaticamente durante o processo de sequenciamento. Quando o pacote é publicado globalmente, a extensão do shell oferece aos usuários a mesma funcionalidade que se o aplicativo fosse instalado localmente. O aplicativo não requer configuração adicional ou configuração no cliente para habilitar a funcionalidade de extensão do Shell.

**Requisitos para usar extensões do Shell:**

-   Os pacotes que contêm extensões de shell inseridas devem ser publicados globalmente.

-   O "" bits "do aplicativo, o Sequencer e o cliente App-V devem corresponder ou as extensões do shell não funcionarão. Por exemplo:

    -   A versão do aplicativo é de 64 bits.

    -   O sequenciador está em execução em um computador de 64 bits.

    -   O pacote está sendo entregue a um computador cliente do App-V do 64-bit.

A tabela a seguir exibe as extensões do shell com suporte.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Manipulação</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Manipulador de menu de contexto</p></td>
<td align="left"><p>Adiciona itens de menu ao menu de contexto. Ele é chamado antes de o menu de contexto ser exibido.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de arrastar e soltar</p></td>
<td align="left"><p>Controla a ação ao clicar com o botão direito do mouse no recurso arrastar-e-soltar e modifica o menu de contexto exibido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de destino soltar</p></td>
<td align="left"><p>Controla a ação após um objeto de dados ser arrastado e solto em um destino de soltura, como um arquivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de objeto de dados</p></td>
<td align="left"><p>Controla a ação após um arquivo ser copiado para a área de transferência ou arrastado e solto em um destino de soltura. Ele pode fornecer formatos de área de transferência adicionais para o destino de soltura.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de folha de propriedades</p></td>
<td align="left"><p>Substitui ou adiciona páginas à caixa de diálogo folha de propriedades de um objeto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador InfoTip</p></td>
<td align="left"><p>Permite a recuperação de sinalizadores e informações de infotip de um item e a exibição dentro de uma dica de ferramenta pop-up ao focalizar o mouse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de colunas</p></td>
<td align="left"><p>Permite criar e exibir colunas personalizadas no modo de exibição de detalhes do Windows Explorer <em> </em> . Ele pode ser usado para estender a classificação e o agrupamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gerenciador de visualização</p></td>
<td align="left"><p>Permite que uma visualização de um arquivo seja exibida no painel de visualização do Windows Explorer.</p></td>
</tr>
</tbody>
</table>

 

### COM

O cliente App-V dá suporte a aplicativos de publicação com suporte para integração COM e virtualização. A integração COM permite que o cliente App-V Registre objetos COM no sistema operacional local e virtualização dos objetos. Para os fins deste documento, a integração de objetos COM requer detalhe adicional.

O App-V oferece suporte ao registro de objetos COM do pacote para o sistema operacional local com dois tipos de processo: fora de processo e em processo. O registro de objetos COM é realizado com uma ou uma combinação de vários modos de operação para um pacote App-V específico que inclui desativado, isolado e integrado. O modo integrado é configurado para o tipo fora de processo ou no processo. A configuração dos modos de COM e tipos é realizada com arquivos de configuração dinâmica (deploymentconfig.xml ou userconfig.xml).

Detalhes sobre a integração do App-V estão disponíveis em: <https://go.microsoft.com/fwlink/?LinkId=392834> .

### Recursos de aplicativos e clientes de software

O App-V dá suporte a clientes de software e pontos de extensão de recursos de aplicativo específicos que permitem que aplicativos virtualizados sejam registrados com o cliente de software do sistema operacional. Isso permite que os usuários selecionem programas padrão para operações como emails, mensagens instantâneas e Media Player. Essa operação é realizada no painel de controle com o botão Definir acesso do programa e padrões do computador e é configurado durante o sequenciamento nos arquivos de manifesto ou de configuração dinâmica. Os recursos do aplicativo só têm suporte quando os aplicativos do App-V são publicados globalmente.

Exemplo de registro de cliente de software de um cliente de email baseado em App-V.

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

**Observação**  Neste exemplo:

-   `<ClientConfiguration EmailEnabled="true" />` é a configuração geral dos clientes de software para integrar clientes de email

-   `<EMail MakeDefault="true">` é o sinalizador para definir um cliente de email específico como o cliente de email padrão

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` é o registro de dll MAPI

 

### Manipulador de protocolo de URL

Os aplicativos nem sempre são chamados de aplicativos virtualizados usando invocação de tipo de arquivo. Por exemplo, em um aplicativo com suporte para inserir um link mailto: dentro de um documento ou página da Web, o usuário clica em um link mailto: e espera obter seu cliente de email registrado. O App-V dá suporte a manipuladores de protocolo de URL que podem ser registrados em cada pacote com o sistema operacional local. Durante o sequenciamento, os manipuladores de protocolo de URL são adicionados automaticamente ao pacote.

Para situações em que há mais de um aplicativo que pode registrar o manipulador de protocolo de URL específico, os arquivos de configuração dinâmica podem ser utilizados para modificar o comportamento e suprimir ou desabilitar esse recurso para um aplicativo que não deve ser o aplicativo principal iniciado.

### AppPath

O ponto de extensão AppPath permite chamar aplicativos App-V diretamente do sistema operacional. Isso normalmente é realizado na tela de execução ou início, dependendo do sistema operacional, que permite que os administradores forneçam acesso a aplicativos App-V de comandos do sistema operacional ou scripts sem chamar o caminho específico para o executável. Portanto, evita modificar a variável de ambiente de caminho do sistema em todos os sistemas, conforme é realizado durante a publicação.

O ponto de extensão AppPath é configurado no manifesto ou nos arquivos de configuração dinâmico e é armazenado no registro do computador local durante a publicação para o usuário. Para obter informações adicionais sobre a revisão do AppPath: <https://go.microsoft.com/fwlink/?LinkId=392835> .

### Aplicativo virtual

Esse subsistema fornece uma lista de aplicativos capturados durante o sequenciamento, que normalmente são consumidos por outros componentes do App-V. A integração de pontos de extensão que pertencem a um aplicativo específico pode ser desabilitada usando arquivos de configuração dinâmico. Por exemplo, se um pacote contém dois aplicativos, é possível desabilitar todos os pontos de extensão pertencentes a um aplicativo, para permitir somente a integração de pontos de extensão de outro aplicativo.

### Regras de ponto de extensão

Os pontos de extensão descritos acima são integrados ao sistema operacional com base na forma como os pacotes foram publicados. Locais de publicação global pontos de extensão em locais de máquinas públicas, onde a publicação do usuário coloca os pontos de extensão nos locais dos usuários. Por exemplo, um atalho criado na área de trabalho e publicado globalmente resultará nos dados de arquivo para o atalho (%Public%\\Desktop) e os dados do registro (HKLM\\Software\\Classes). O mesmo atalho teria dados de arquivo (%UserProfile%\\Desktop) e dados do registro (HKCU\\Software\\Classes).

Os pontos de extensão não são todos publicados da mesma maneira, em que alguns pontos de extensão exigirão publicação global e outros exigem sequenciamento no sistema operacional específico e na arquitetura onde são entregues. Veja a seguir uma tabela que descreve essas duas principais regras.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Extensão virtual</th>
<th align="left">Requer o sequenciamento de so de destino</th>
<th align="left">Requer publicação global</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Atalho</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Associação de tipo de arquivo</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protocolos de URL</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppPaths</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modo COM</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de software</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Funcionalidades do aplicativo</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de menu de contexto</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de arrastar e soltar</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de objeto de dados</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de folha de propriedades</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador InfoTip</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de colunas</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Extensões do Shell</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Objeto auxiliar do navegador</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Objeto ActiveX</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a>Processamento dinâmico de configuração


Implantar pacotes do App-V em um computador ou usuário é muito simples. No entanto, como as organizações implantam aplicativos do AppV em linhas comerciais e limites geográficos e políticos, a capacidade de sequenciar um aplicativo uma vez com um conjunto de configurações se torna impossível. O App-V foi projetado para esse cenário, pois ele captura configurações e configurações específicas durante o sequenciamento no arquivo de manifesto, mas também dá suporte à modificação com arquivos de configuração dinâmicos.

A configuração dinâmica do App-V permite especificar uma política para um pacote no nível do computador ou no nível do usuário. Os arquivos de configuração dinâmica permitem que os engenheiros de sequenciamento modifiquem a configuração de um pacote, seqüência de postagem, para atender às necessidades de grupos individuais de usuários ou máquinas. Em alguns casos, pode ser necessário fazer modificações no aplicativo para fornecer a funcionalidade adequada dentro do ambiente do App-V. Por exemplo, talvez seja necessário fazer modificações nos arquivos \ _ \ * config.xml para permitir que determinadas ações sejam executadas em um tempo especificado durante a execução do aplicativo, como desabilitar uma extensão mailto para impedir que um aplicativo virtualizado Substitua essa extensão de outro aplicativo.

Os pacotes do App-V contêm o arquivo de manifesto dentro do arquivo do pacote do AppV, que é o representativo de operações de sequenciamento e é a política escolhida, a menos que arquivos de configuração dinâmicos sejam atribuídos a um pacote específico. Pós-sequenciamento, os arquivos de configuração dinâmica podem ser modificados para permitir a publicação de um aplicativo para áreas de trabalho ou usuários diferentes com pontos de extensão diferentes. Os dois arquivos de configuração dinâmica são os arquivos DDC (configuração de implantação dinâmica) e DUC (configuração dinâmica do usuário). Esta seção enfoca a combinação dos arquivos de manifesto e de configuração dinâmica.

### Exemplo de arquivos de configuração dinâmicos

O exemplo a seguir mostra a combinação dos arquivos de manifesto, configuração de implantação e configuração do usuário após a publicação e durante a operação normal. Estes exemplos são exemplos abreviados de cada um dos arquivos. O objetivo é mostrar a combinação apenas dos arquivos e não ser uma descrição completa das categorias específicas disponíveis em cada um dos arquivos. Para obter mais informações, consulte o guia de sequenciamento do App-V 5 em: <https://go.microsoft.com/fwlink/?LinkID=269810>

**Manifesto**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**Configuração de implantação**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**Configuração do usuário**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a>Montagens lado a lado


O App-V dá suporte ao empacotamento automático de assemblies lado a lado (SxS) durante o sequenciamento e a implantação no cliente durante a publicação do aplicativo virtual. O App-V 5 SP2 dá suporte à captura de assemblies SxS durante o sequenciamento para assemblies que não estão presentes na máquina de sequenciamento. E para assemblies que consistem em Visual C++ (versão 8 e mais recente) e/ou em tempo de execução do MSXML, o sequenciador detectará e capturará essas dependências automaticamente, mesmo que elas não tenham sido instaladas durante o monitoramento. O recurso de assemblies lado a lado remove as limitações das versões anteriores do App-V, em que o sequenciador do App-V não captura assemblies já presentes na estação de trabalho de sequenciamento e privatizing os assemblies que limitam-se a uma versão de bit por pacote. Esse comportamento resultou em aplicativos do App-V implantados em clientes que não continham os assemblies SxS necessários, causando falhas de inicialização do aplicativo. Isso forçou o processo de empacotamento para documentar e, em seguida, garantir que todos os assemblies necessários para pacotes foram instalados localmente no sistema operacional cliente do usuário para garantir o suporte para os aplicativos virtuais. Com base no número de assemblies e na falta de documentação do aplicativo para as dependências necessárias, essa tarefa foi um desafio de gerenciamento e implementação.

O suporte ao assembly lado a lado do App-V tem os recursos a seguir.

-   Capturas automáticas do assembly SxS durante o sequenciamento, independentemente de o assembly já ter sido instalado na estação de trabalho de sequenciamento.

-   O cliente App-V instala automaticamente assemblies SxS necessários para o computador cliente no momento da publicação, quando eles não estão presentes.

-   O sequenciador relata a dependência do tempo de execução do VC no mecanismo de relatório do sequenciador.

-   O sequenciador permite optar por não empacotar os assemblies que já estão instalados no sequenciador, oferecendo suporte a cenários em que os assemblies foram instalados anteriormente nos computadores de destino.

### Publicação automática de assemblies SxS

Durante a publicação de um pacote App-V com assemblies SxS, o cliente App-V Verifica a presença do assembly na máquina. Se o assembly não existir, o cliente vai implantar o assembly na máquina. Os pacotes que fazem parte dos grupos de conexão dependerão das instalações de assembly lado a lado que fazem parte dos pacotes base, pois o grupo de conexões não contém informações sobre a instalação do assembly.

**Observação**  Cancelar a publicação ou a remoção de um pacote com um assembly não remove os assemblies desse pacote.

 

## <a href="" id="bkmk-client-logging"></a>Registro em log do cliente


O cliente App-V registra informações no log de eventos do Windows no formato ETW padrão. Os eventos específicos do App-V podem ser encontrados no Visualizador de eventos, em aplicativos e serviços Logs\\Microsoft\\AppV\\Client.

**Observação**  No App-V 5,0 SP3, alguns registros foram consolidados e movidos para o seguinte local:

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Para obter uma lista dos logs movidos, consulte [sobre o App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

 

Há três categorias específicas de eventos gravadas descritas abaixo.

**Administrador**: registra eventos para configurações aplicadas ao cliente App-V e contém os principais avisos e erros.

**Operacional**: registra a execução geral do App-v e o uso de componentes individuais criando um log de auditoria das operações do App-v que foram concluídas no cliente App-v.

**Aplicativo virtual**: registra os lançamentos e o uso de subsistemas de virtualização do aplicativo virtual.






 

 





