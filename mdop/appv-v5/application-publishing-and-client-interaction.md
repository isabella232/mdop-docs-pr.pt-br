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
ms.openlocfilehash: fb648db11009d6f3331d68c5fb8ba74b578fa52c
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910836"
---
# <a name="application-publishing-and-client-interaction"></a>Publicação de aplicativos e interação com clientes


Este artigo fornece informações técnicas sobre operações comuns do cliente App-V e sua integração com o sistema operacional local.

-   [Arquivos de pacote do App-V criados pelo Sequencer](#bkmk-appv-pkg-files-list)

-   [O que há no arquivo appv?](#bkmk-appv-file-contents)

-   [Locais de armazenamento de dados do cliente app-V](#bkmk-files-data-storage)

-   [Registro de pacote](#bkmk-pkg-registry)

-   [Comportamento do armazenamento de pacotes do App-V](#bkmk-pkg-store-behavior)

-   [Registro e dados de roaming](#bkmk-roaming-reg-data)

-   [Gerenciamento do ciclo de vida do aplicativo cliente app-V](#bkmk-clt-app-lifecycle)

-   [Integração de pacotes do App-V](#bkmk-integr-appv-pkgs)

-   [Processamento de configuração dinâmica](#bkmk-dynamic-config)

-   [Assemblies lado a lado](#bkmk-sidebyside-assemblies)

-   [Log do cliente](#bkmk-client-logging)

Para obter informações de referência adicionais, consulte [Microsoft Application Virtualization (App-V) Documentation Resources Download Page](https://www.microsoft.com/download/details.aspx?id=27760).

## <a name="app-v-package-files-created-by-the-sequencer"></a><a href="" id="bkmk-appv-pkg-files-list"></a>Arquivos de pacote do App-V criados pelo Sequencer


O Sequencer cria pacotes do App-V e produz um aplicativo virtualizado. O processo de sequenciamento cria os seguintes arquivos:

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
<td align="left"><p>.appv</p></td>
<td align="left"><ul>
<li><p>O arquivo de pacote principal, que contém os ativos capturados e informações de estado do processo de sequenciamento.</p></li>
<li><p>Arquitetura do arquivo de pacote, informações de publicação e registro em um formulário tokenizado que pode ser reaplicado a um computador e a um usuário específico após a entrega.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>.MSI</p></td>
<td align="left"><p>Wrapper de implantação executável que você pode usar para implantar arquivos .appv manualmente ou usando uma plataforma de implantação de terceiros.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>_DeploymentConfig.XML</p></td>
<td align="left"><p>Arquivo usado para personalizar os parâmetros de publicação padrão para todos os aplicativos em um pacote implantado globalmente para todos os usuários em um computador que está executando o cliente App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>_UserConfig.XML</p></td>
<td align="left"><p>Arquivo usado para personalizar os parâmetros de publicação de todos os aplicativos em um pacote implantado para um usuário específico em um computador que está executando o cliente App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Report.xml</p></td>
<td align="left"><p>Resumo das mensagens resultantes do processo de sequenciamento, incluindo drivers, arquivos e locais do Registro omitidos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>.CAB</p></td>
<td align="left"><p><em>Opcional: Arquivo acelerador de pacote usado para recriar automaticamente um pacote de aplicativo virtual previamente </em> sequenciado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>.appvt</p></td>
<td align="left"><p><em>Opcional: </em> arquivo de modelo sequencer usado para reter as configurações do Sequencer comumente reutilizados.</p></td>
</tr>
</tbody>
</table>

 

Para obter informações sobre sequenciamento, consulte [Application Virtualization 5.0 Sequencing Guide](https://www.microsoft.com/download/details.aspx?id=27760).

## <a name="whats-in-the-appv-file"></a><a href="" id="bkmk-appv-file-contents"></a>O que há no arquivo appv?


O arquivo appv é um contêiner que armazena arquivos XML e não XML juntos em uma única entidade. Esse arquivo é criado a partir do formato AppX, que se baseia no padrão Open Packaging Conventions (OPC).

Para exibir o conteúdo do arquivo appv, faça uma cópia do pacote e renomeie o arquivo copiado para uma extensão ZIP.

O arquivo appv contém a seguinte pasta e arquivos, que são usados ao criar e publicar um aplicativo virtual:

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
<td align="left"><p>Diretório que contém o sistema de arquivos do aplicativo virtualizado que é capturado durante a sequenciamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>[Content_Types].xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Lista dos principais tipos de conteúdo no arquivo appv (por exemplo, DLL, EXE, BIN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppxBlockMap.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Layout do arquivo appv, que usa elementos File, Block e BlockMap que permitem a localização e validação de arquivos no pacote app-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AppxManifest.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Metadados para o pacote que contém as informações necessárias para adicionar, publicar e iniciar o pacote. Inclui pontos de extensão (associações de tipos de arquivo e atalhos) e os nomes e GUIDs associados ao pacote.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FilesystemMetadata.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Lista dos arquivos capturados durante a sequenciamento, incluindo atributos (por exemplo, diretórios, arquivos, diretórios opacos, diretórios vazios e nomes longos e curtos).</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageHistory.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Informações sobre o computador de sequenciamento (versão do sistema operacional, versão do Internet Explorer, versão do .Net Framework) e processo (atualização, versão do pacote).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registry.dat</p></td>
<td align="left"><p>Arquivo DAT</p></td>
<td align="left"><p>Chaves e valores do Registro capturados durante o processo de sequenciamento do pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>StreamMap.xml</p></td>
<td align="left"><p>Arquivo XML</p></td>
<td align="left"><p>Lista de arquivos para o bloco de recursos primário e de publicação. O bloco de recursos de publicação contém os arquivos ICO e partes necessárias de arquivos (EXE e DLL) para publicação do pacote. Quando presente, o bloco de recursos principal inclui arquivos que foram otimizados para streaming durante o processo de sequenciamento.</p></td>
</tr>
</tbody>
</table>

 

## <a name="app-v-client-data-storage-locations"></a><a href="" id="bkmk-files-data-storage"></a>Locais de armazenamento de dados do cliente app-V


O cliente App-V executa tarefas para garantir que os aplicativos virtuais sejam executados corretamente e funcionem como aplicativos instalados localmente. O processo de abertura e execução de aplicativos virtuais requer mapeamento do sistema de arquivos virtuais e do Registro para garantir que o aplicativo tenha os componentes necessários de um aplicativo tradicional esperado pelos usuários. Esta seção descreve os ativos necessários para executar aplicativos virtuais e lista o local onde o App-V armazena os ativos.

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
<td align="left"><p>Package Store</p></td>
<td align="left"><p>%ProgramData%\App-V</p></td>
<td align="left"><p>Local padrão para arquivos de pacote somente leitura</p></td>
</tr>
<tr class="even">
<td align="left"><p>Catálogo de Máquinas</p></td>
<td align="left"><p>%ProgramData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contém documentos de configuração por máquina</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Catálogo de Usuários</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Catalog</p></td>
<td align="left"><p>Contém documentos de configuração por usuário</p></td>
</tr>
<tr class="even">
<td align="left"><p>Backups de atalho</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</p></td>
<td align="left"><p>Armazena pontos de integração anteriores que permitem a restauração no pacote não publicado</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Copiar em Gravar (VACA) Roaming</p></td>
<td align="left"><p>%AppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Local de roaming writeable para modificação do pacote</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copiar em Gravar (VACA) Local</p></td>
<td align="left"><p>%LocalAppData%\Microsoft\AppV\Client\VFS</p></td>
<td align="left"><p>Local não roaming que pode ser escrito para modificação do pacote</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registro de Máquina</p></td>
<td align="left"><p>HKLM\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contém informações de estado do pacote, incluindo VReg para pacotes de máquina ou publicados globalmente (Hive do computador)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registro do Usuário</p></td>
<td align="left"><p>HKCU\Software\Microsoft\AppV</p></td>
<td align="left"><p>Contém informações de estado do pacote do usuário, incluindo VReg</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Classes de Registro de Usuário</p></td>
<td align="left"><p>HKCU\Software\Classes\AppV</p></td>
<td align="left"><p>Contém informações adicionais de estado do pacote do usuário</p></td>
</tr>
</tbody>
</table>

 

Detalhes adicionais para a tabela são fornecidos na seção abaixo e em todo o documento.

### <a name="package-store"></a>Armazenamento de pacotes

O Cliente app-V gerencia os ativos de aplicativos montados no armazenamento de pacotes. Esse local de armazenamento padrão é , mas você pode configurá-lo durante ou após a instalação usando o comando `%ProgramData%\App-V` do PowerShell, que modifica o registro local ( valor sob `Set-AppVClientConfiguration` `PackageInstallationRoot` a `HKLM\Software\Microsoft\AppV\Client\Streaming` chave). O armazenamento do pacote deve estar localizado em um caminho local no sistema operacional cliente. Os pacotes individuais são armazenados no armazenamento de pacotes em subdireções nomeados para o GUID do pacote e o GUID da versão.

Exemplo de um caminho para um aplicativo específico:

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

Para alterar o local padrão do armazenamento de pacotes durante a instalação, consulte [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md).

### <a name="shared-content-store"></a>Armazenamento de Conteúdo Compartilhado

Se o Cliente do App-V estiver configurado no modo Armazenamento de Conteúdo Compartilhado, nenhum dado será gravado no disco quando ocorrer uma falha de fluxo, o que significa que os pacotes exigem espaço em disco local mínimo (dados de publicação). O uso de menos espaço em disco é altamente desejável em ambientes VDI, onde o armazenamento local pode ser limitado, e o streaming dos aplicativos de um local de rede de alto desempenho (como san) é preferível. Para obter mais informações sobre o modo de armazenamento de conteúdo compartilhado, consulte <https://go.microsoft.com/fwlink/p/?LinkId=392750> .

**Observação**  
O computador e o armazenamento de pacotes devem estar localizados em uma unidade local, mesmo quando você estiver usando configurações da Loja de Conteúdo Compartilhado para o Cliente app-V.

 

### <a name="package-catalogs"></a>Catálogos de pacotes

O Cliente App-V gerencia os dois locais baseados em arquivo a seguir:

-   **Catálogos (usuário e máquina).**

-   **Locais do Registro** - depende de como o pacote é direcionado para publicação. Há um Catálogo (armazenamento de dados) para o computador e um catálogo para cada usuário individual. O Catálogo de Máquinas armazena informações globais aplicáveis a todos os usuários ou a qualquer usuário, e o Catálogo de Usuários armazena informações aplicáveis a um usuário específico. O Catálogo é uma coleção de configurações dinâmicas e arquivos de manifesto; há dados discretos para o arquivo e o Registro por versão do pacote. 

### <a name="machine-catalog"></a>Catálogo de máquinas

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Armazena documentos de pacote que estão disponíveis para os usuários no computador, quando pacotes são adicionados e publicados. No entanto, se um pacote for "global" no momento da publicação, as integrações estarão disponíveis para todos os usuários.</p>
<p>Se um pacote não for global, as integrações serão publicadas apenas para usuários específicos, mas ainda há recursos globais que são modificados e visíveis para qualquer pessoa no computador cliente (por exemplo, o diretório do pacote está em um local de disco compartilhado).</p>
<p>Se um pacote estiver disponível para um usuário no computador (global ou não global), o manifesto será armazenado no Catálogo de Máquinas. Quando um pacote é publicado globalmente, há um arquivo de Configuração Dinâmica, armazenado no Catálogo de Máquinas; portanto, a determinação de se um pacote é global é definida de acordo com se há um arquivo de política (arquivo UserDeploymentConfiguration) no Catálogo de Máquinas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Local de armazenamento padrão</p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p>Esse local não é o mesmo que o local do Package Store. O Package Store é a cópia dourada ou perfeita dos arquivos do pacote.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivos no catálogo de máquinas</p></td>
<td align="left"><ul>
<li><p>Manifest.xml</p></li>
<li><p>DeploymentConfiguration.xml</p></li>
<li><p>UserManifest.xml (Pacote Publicado Globalmente)</p></li>
<li><p>UserDeploymentConfiguration.xml (Pacote Publicado Globalmente)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Local adicional do catálogo de máquinas, usado quando o pacote faz parte de um grupo de conexão</p></td>
<td align="left"><p>O seguinte local é, além do local de pacote específico mencionado acima:</p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivos adicionais no catálogo de máquinas quando o pacote faz parte de um grupo de conexão</p></td>
<td align="left"><ul>
<li><p>PackageGroupDescriptor.xml</p></li>
<li><p>UserPackageGroupDescriptor.xml (grupo de conexão publicado globalmente)</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="user-catalog"></a>Catálogo de usuários

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Descrição</p></td>
<td align="left"><p>Criado durante o processo de publicação. Contém informações usadas para publicar o pacote e também usadas no início para garantir que um pacote seja provisionado para um usuário específico. Criado em um local de roaming e inclui informações de publicação específicas do usuário.</p>
<p>Quando um pacote é publicado para um usuário, o arquivo de política é armazenado no Catálogo de Usuários. Ao mesmo tempo, uma cópia do manifesto também é armazenada no Catálogo de Usuários. Quando um direito de pacote é removido para um usuário, os arquivos de pacote relevantes são removidos do Catálogo de Usuários. Ao olhar para o catálogo de usuários, um administrador pode exibir a presença de um arquivo de Configuração Dinâmica, o que indica que o pacote tem direito a esse usuário.</p>
<p>Para usuários móveis, o Catálogo de Usuários precisa estar em um local roaming ou compartilhado para preservar o comportamento herdado do App-V de direcionar usuários por padrão. O direito e a política estão vinculados a um usuário, não a um computador, portanto, eles devem circular com o usuário depois que eles são provisionados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Local de armazenamento padrão</p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivos no catálogo de usuários</p></td>
<td align="left"><ul>
<li><p>UserManifest.xml</p></li>
<li><p>DynamicConfiguration.xml ou UserDeploymentConfiguration.xml</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Local adicional do catálogo de usuários, usado quando o pacote faz parte de um grupo de conexão</p></td>
<td align="left"><p>O seguinte local é, além do local de pacote específico mencionado acima:</p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquivo adicional no catálogo de máquinas quando o pacote faz parte de um grupo de conexão</p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <a name="shortcut-backups"></a>Backups de atalho

Durante o processo de publicação, o Cliente app-V faz backup de todos os atalhos e pontos de integração para Esse backup permite a restauração desses pontos de integração para as versões anteriores quando o pacote é `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` não publicado.

### <a name="copy-on-write-files"></a>Copiar em Arquivos de gravação

O Package Store contém uma cópia perfeita dos arquivos de pacote que foram transmitidos do servidor de publicação. Durante a operação normal de um aplicativo App-V, o usuário ou serviço pode exigir alterações nos arquivos. Essas alterações não são feitas no armazenamento de pacotes para preservar sua capacidade de reparar o aplicativo, o que remove essas alterações. Esses locais, chamados de Copiar em Gravação (VACA), suportam locais roaming e não roaming. O local onde as modificações são armazenadas depende de onde o aplicativo foi programado para gravar alterações em uma experiência nativa.

### <a name="cow-roaming"></a>Roaming DE VACA

O local de Roaming DE VACA descrito acima armazena alterações em arquivos e diretórios direcionados para o local %AppData% típico ou \\Users\\{username}\\AppData\\Local de roaming. Esses diretórios e arquivos são então roamed com base nas configurações do sistema operacional.

### <a name="cow-local"></a>LOCAL DE VACA

O local LOCAL DA VACA é semelhante ao local de roaming, mas os diretórios e arquivos não são roamed para outros computadores, mesmo que o suporte a roaming tenha sido configurado. O local LOCAL DA VACA descrito acima armazena as alterações aplicáveis às janelas típicas e não à localização %AppData%. Os diretórios listados variarão, mas haverá dois locais para qualquer Windows locais típicos (por exemplo, AppData Comum e Common AppDataS). O **S** significa o local restrito quando o serviço virtual solicita a alteração como um usuário com nível elevado diferente dos usuários conectados. O local não**S** armazena alterações baseadas no usuário.

## <a name="package-registry"></a><a href="" id="bkmk-pkg-registry"></a>Registro de pacote


Antes que um aplicativo possa acessar os dados do registro do pacote, o Cliente App-V deve disponibilizar os dados do registro do pacote para os aplicativos. O Cliente App-V usa o registro real como um armazenamento de backing para todos os dados do Registro.

Quando um novo pacote é adicionado ao Cliente App-V, uma cópia do REGISTRO. O arquivo DAT do pacote é criado em `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` . O nome do arquivo é o GUID da versão com o . Extensão DAT. O motivo pelo qual essa cópia é feita é para garantir que o arquivo hive real no pacote nunca está em uso, o que impediria a remoção do pacote posteriormente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Registry.dat do Package Store</strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong>%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</strong></p></td>
</tr>
</tbody>
</table>

 

Quando o primeiro aplicativo do pacote é lançado no cliente, o cliente estágios ou copia o conteúdo do arquivo hive, criando os dados do registro do pacote em um local alternativo `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` . Os dados do Registro em estágios têm dois tipos distintos de dados do computador e dados do usuário. Os dados do computador são compartilhados em todos os usuários no computador. Os dados do usuário são em estágios para cada usuário para um local específico do `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` usuário. Os dados do computador são removidos no momento da remoção do pacote e os dados do usuário são removidos em uma operação de não publicação do usuário.

### <a name="package-registry-staging-vs-connection-group-registry-staging"></a>Preparação do registro do pacote versus preparação do registro do grupo de conexão

Quando os grupos de conexão estão presentes, o processo anterior de preparação do Registro se mantém verdadeiro, mas, em vez de ter um arquivo de hive para processar, há mais de um. Os arquivos são processados na ordem em que aparecem no grupo de conexão XML, com o primeiro escritor vencendo quaisquer conflitos.

O Registro em estágios persiste da mesma forma que no caso do pacote único. Os dados do registro do usuário em estágios permanecem para o grupo de conexão até que eles são desabilitados; Os dados do registro do computador em estágios são removidos na remoção do grupo de conexão.

### <a name="virtual-registry"></a>Registro virtual

O objetivo do registro virtual (VREG) é fornecer uma única exibição mesclada do registro do pacote e do registro nativo para aplicativos. Ele também fornece a funcionalidade de cópia ao gravar (VACA) – ou seja, todas as alterações feitas no Registro a partir do contexto de um processo virtual são feitas em um local DE VACA separado. Isso significa que o VREG deve combinar até três locais de registro separados em um único exibição com base nos locais preenchidos no REGISTRO DESAD - pacote &gt; - &gt; nativo. Quando uma solicitação é feita para um registro de dados, ela será localizada em ordem até encontrar os dados que estava solicitando. Ou seja, se houver um valor armazenado em um local DESAD, ele não prosseguirá para outros locais, no entanto, se não houver dados no local DE VACA, ele prosseguirá para o Pacote e, em seguida, para o local nativo até encontrar os dados apropriados.

### <a name="registry-locations"></a>Locais do Registro

Há dois locais de registro de pacote e dois locais de grupo de conexão em que o cliente App-V armazena informações do Registro, dependendo se o Pacote é publicado individualmente ou como parte de um grupo de conexão. Há três locais DE VACA para pacotes e três para grupos de conexão, que são criados e gerenciados pelo VREG. Configurações pacotes e grupos de conexão não são compartilhados:

**VReg de Pacote Único:**

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
<li><p>Registro de Máquina\Cliente\Pacotes\PkgGUID\REGISTRY (Somente o processo de elevação pode gravar)</p></li>
<li><p>Registro do Usuário\Cliente\Pacotes\PkgGUID\REGISTRO (User Roaming qualquer coisa escrita em HKCU, exceto Software\Classes</p></li>
<li><p>Classes do Registro do Usuário\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes grava e HKLM para processo não elevado)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Pacote</strong></p></td>
<td align="left"><ul>
<li><p>Registro de Máquina\Cliente\Pacotes\PkgGUID\Versions\VerGuid\Registry\Machine</p></li>
<li><p>Classes do Registro do Usuário\Client\Packages\PkgGUID\Versions\VerGUID\Registry</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nativo</strong></p></td>
<td align="left"><ul>
<li><p>Local do registro de aplicativo nativo</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**VReg do Grupo de Conexão:**

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
<li><p>Registro de Máquina\Cliente\PackageGroups\GrpGUID\REGISTRY (somente o processo de elevação pode gravar)</p></li>
<li><p>Registro do Usuário\Cliente\PackageGroups\GrpGUID\REGISTRY (Qualquer coisa escrita no HKCU, exceto Software\Classes</p></li>
<li><p>Classes do Registro do Usuário\Client\PackageGroups\GrpGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Pacote</strong></p></td>
<td align="left"><ul>
<li><p>Registro de Máquina\Cliente\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
<li><p>Classes do Registro do Usuário\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nativo</strong></p></td>
<td align="left"><ul>
<li><p>Local do registro de aplicativo nativo</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

Há dois locais DESAD para HKLM; processos elevados e não elevados. Os processos elevados sempre escrevem alterações HKLM no VACA seguro em HKLM. Os processos não elevados sempre escrevem alterações de HKLM no VACA não seguro em HKCU\\Software\\Classes. Quando um aplicativo lê as alterações do HKLM, os processos elevados lerão as alterações do VACA seguro em HKLM. Leituras não elevadas de ambos, favorecendo as alterações feitas na VACA não declarada primeiro.

### <a name="pass-through-keys"></a>Chaves de passagem

As chaves de passagem permitem que um administrador configure determinadas chaves para que elas só possam ser lidas do Registro nativo, ignorando os locais Package e COW. Os locais de passagem são globais no computador (não são específicos do pacote) e podem ser configurados adicionando o caminho à chave, que deve ser tratado como passagem para o **valor REG\_MULTI\_SZ** chamado **PassThroughPaths** da chave `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` . Qualquer chave que aparece sob esse valor de cadeia de caracteres (e seus filhos) será tratada como passagem.

Os seguintes locais são configurados como locais de passagem por padrão:

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Configurações\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Configurações\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application

-   HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Configurações

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib

-   HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies

-   HKEY\_CURRENT\_USER\\SOFTWARE\\Policies

O objetivo das chaves de passagem é garantir que um aplicativo virtual não escreva dados do Registro no VReg necessário para aplicativos não virtuais para uma operação ou integração bem-sucedida. A chave Políticas garante que as configurações baseadas na Política de Grupo definidas pelo administrador sejam usadas e não por configurações de pacote. A chave AppModel é necessária para integração com Windows aplicativos baseados na interface do usuário moderna. É recomendável que as administrações não modifiquem nenhuma das chaves de passagem padrão, mas, em algumas instâncias, com base no comportamento do aplicativo podem exigir a adição de chaves de passagem adicionais.

## <a name="app-v-package-store-behavior"></a><a href="" id="bkmk-pkg-store-behavior"></a>Comportamento do armazenamento de pacotes do App-V


O App-V 5 gerencia o Package Store, que é o local onde os arquivos de ativos expandidos do arquivo appv são armazenados. Por padrão, esse local é armazenado em %ProgramData%\\App-V e é limitado em termos de recursos de armazenamento apenas por espaço em disco gratuito. O armazenamento de pacotes é organizado pelos GUIDs para o pacote e a versão, conforme mencionado na seção anterior.

### <a name="add-packages"></a>Adicionar pacotes

Os Pacotes do App-V são em estágios após a adição ao computador com o Cliente App-V. O Cliente App-V fornece preparação sob demanda. Durante a publicação ou um Add-AppVClientPackage manual, a estrutura de dados é criada no armazenamento de pacotes (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}). Os arquivos de pacote identificados no bloco de publicação definido no StreamMap.xml são adicionados ao sistema e as pastas de nível superior e arquivos filho em estágios para garantir que os ativos apropriados do aplicativo existam no início.

### <a name="mounting-packages"></a>Pacotes de montagem

Os pacotes podem ser carregados explicitamente usando o PowerShell ou usando a interface do usuário do cliente `Mount-AppVClientPackage` **App-V** para baixar um pacote. Essa operação carrega completamente o pacote inteiro no armazenamento de pacotes.

### <a name="streaming-packages"></a>Pacotes de streaming

O Cliente App-V pode ser configurado para alterar o comportamento padrão de streaming. Todas as políticas de streaming são armazenadas sob a seguinte chave do Registro: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` . As políticas são definidas usando o cmdlet do PowerShell `Set-AppvClientConfiguration` . As seguintes políticas se aplicam ao Streaming:

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
<td align="left"><p>No Windows 8 permite streaming em redes 3G e celulares</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>Especifica a configuração De carga em segundo plano:</p>
<p><strong>0 </strong> - Desabilitado</p>
<p><strong>1 </strong> – Somente pacotes usados anteriormente</p>
<p><strong>2 </strong> – Todos os Pacotes</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>A pasta raiz do armazenamento de pacotes no computador local</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>A substituição raiz de onde os pacotes devem ser transmitidos de</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>Habilita o uso do Armazenamento de Conteúdo Compartilhado para cenários VDI</p></td>
</tr>
</tbody>
</table>

 

 

Essas configurações afetam o comportamento dos ativos de pacote do App-V de streaming para o cliente. Por padrão, o App-V só baixa os ativos necessários depois de baixar os blocos de recursos primários e de publicação inicial. Há três comportamentos específicos em torno de pacotes de streaming que devem ser explicados:

-   Streaming em segundo plano

-   Streaming otimizado

-   Falhas de fluxo

### <a name="background-streaming"></a>Streaming em segundo plano

O cmdlet do PowerShell pode ser usado para determinar o modo atual para streaming em segundo plano com a configuração de Carregamento Automático e modificado com o cmdlet Set-AppvClientConfiguration ou do Registro `Get-AppvClientConfiguration` (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key). Streaming em segundo plano é uma configuração padrão em que a configuração de Carregamento Automático é definida para baixar pacotes usados anteriormente. O comportamento com base na configuração padrão (value=1) baixa os blocos de dados do App-V em segundo plano depois que o aplicativo é lançado. Essa configuração pode ser desabilitada em conjunto (valor=0) ou habilitada para todos os pacotes (valor=2), se eles foram lançados.

### <a name="optimized-streaming"></a>Streaming otimizado

Os pacotes do App-V podem ser configurados com um bloco de recursos principal durante a sequenciamento. Essa configuração permite que o engenheiro de sequenciamento monitore arquivos de início para um aplicativo ou aplicativo específico e marque os blocos de dados no pacote app-V para streaming no início de qualquer aplicativo no pacote.

### <a name="stream-faults"></a>Falhas de fluxo

Após o fluxo inicial de todos os dados de publicação e o bloco de recursos primários, as solicitações de arquivos adicionais executam falhas de fluxo. Esses blocos de dados são baixados para o armazenamento de pacotes conforme necessário. Isso permite que um usuário baixe apenas uma pequena parte do pacote, normalmente o suficiente para iniciar o pacote e executar tarefas normais. Todos os outros blocos são baixados quando um usuário inicia uma operação que requer dados que não estão no armazenamento de pacotes.

Para obter mais informações sobre a visita de streaming de pacote do App-V: <https://go.microsoft.com/fwlink/?LinkId=392770> .

A sequenciamento para otimização de streaming está disponível em: <https://go.microsoft.com/fwlink/?LinkId=392771> .

### <a name="package-upgrades"></a>Atualizações de pacote

Os Pacotes do App-V exigem atualização durante todo o ciclo de vida do aplicativo. As atualizações do pacote do App-V são semelhantes à operação de publicação de pacote, pois cada versão será criada em seu próprio local PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` . A operação de atualização é otimizada criando links rígidos para arquivos idênticos e transmitidos de outras versões do mesmo pacote.

### <a name="package-removal"></a>Remoção de pacote

O comportamento do Cliente App-V quando os pacotes são removidos depende do método usado para remoção. Usando uma infraestrutura completa do App-V para não publicar o aplicativo, os arquivos de catálogo de usuários (catálogo de máquinas para aplicativos publicados globalmente) são removidos, mas mantém o local do armazenamento de pacotes e os locais DODS. Quando o cmdlet do PowerShell `Remove-AppVClientPackge` é usado para remover um Pacote do App-V, o local do armazenamento do pacote é limpo. Lembre-se de que a não publicação de um Pacote app-V do Servidor de Gerenciamento não executa uma operação Remover. Nenhuma das operações removerá os arquivos de pacote do Package Store.

## <a name="roaming-registry-and-data"></a><a href="" id="bkmk-roaming-reg-data"></a>Registro e dados de roaming


O App-V 5 é capaz de fornecer uma experiência quase nativa ao roaming, dependendo de como o aplicativo que está sendo usado é gravado. Por padrão, o App-V roams AppData que é armazenado no local de roaming, com base na configuração de roaming do sistema operacional. Outros locais para armazenamento de dados baseados em arquivo não circulam de computador para computador, pois estão em locais que não são roamed.

### <a name="roaming-requirements-and-user-catalog-data-storage"></a><a href="" id="bkmk-clt-inter-roam-reqs"></a>Requisitos de roaming e armazenamento de dados de catálogo de usuários

O App-V armazena dados, que representa o estado do catálogo do usuário, na forma de:

-   Arquivos em %appdata%\\Microsoft\\AppV\\Client\\Catalog

-   Configurações do Registro em `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

Juntos, esses arquivos e configurações do Registro representam o catálogo do usuário, portanto, ambos devem ser roamed ou nenhum deles deve ser roamed para um determinado usuário. O App-V não dá suporte a roaming %AppData%, mas não roaming do perfil do usuário (Registro) ou vice-versa.

**Observação**  
O cmdlet **Repair-AppvClientPackage** não repara o estado de publicação de pacotes, em que o estado do App-V do usuário está ausente ou não está incomparável com os dados em `HKEY_CURRENT_USER` %appdata%.

 

### <a name="registry-based-data"></a>Dados baseados no Registro

O roaming do Registro do App-V se enquadra em dois cenários, conforme mostrado na tabela a seguir.

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
<td align="left"><p>Aplicativos executados como usuários padrão</p></td>
<td align="left"><p>Quando um usuário padrão inicia um aplicativo App-V, HKLM e HKCU para aplicativos App-V são armazenados no hive HKCU no computador. Isso apresenta como dois caminhos distintos:</p>
<ul>
<li><p>HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</p></li>
</ul>
<p>Os locais estão habilitados para roaming com base nas configurações do sistema operacional.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicativos executados com elevação</p></td>
<td align="left"><p>Quando um aplicativo é lançado com elevação:</p>
<ul>
<li><p>Os dados HKLM são armazenados no hive HKLM no computador local</p></li>
<li><p>Os dados HKCU são armazenados no local do Registro do Usuário</p></li>
</ul>
<p>Nesse cenário, essas configurações não são roamed com configurações normais de roaming do sistema operacional, e as chaves e valores do Registro resultantes são armazenados no seguinte local:</p>
<ul>
<li><p>HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</p></li>
<li><p>HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registro\User{UserSID}\SOFTWARE</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <a name="app-v-and-folder-redirection"></a>Redirecionamento de pasta e app-V

O App-V 5.0 SP2 dá suporte ao redirecionamento de pasta da pasta AppData móveis (%AppData%). Quando o ambiente virtual é iniciado, o estado de AppData móveis do diretório AppData móveis do usuário é copiado para o cache local. Por outro lado, quando o ambiente virtual é desligado, o cache local associado ao AppData roaming de um usuário específico é transferido para o local real do diretório AppData roaming desse usuário.

Um pacote típico tem vários locais mapeados no armazenamento de backing do usuário para configurações em AppData\\Local e AppData\\Roaming. Esses locais são os locais Copiar em Gravação armazenados por usuário no perfil do usuário e que são usados para armazenar alterações feitas nos diretórios VFS do pacote e para proteger o VFS do pacote padrão.

A tabela a seguir mostra locais e locais de roaming, quando o redirecionamento de pasta não foi implementado.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Diretório VFS no pacote</th>
<th align="left">Local mapeado do armazenamento de backing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Roaming </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

A tabela a seguir mostra locais e roaming, quando o redirecionamento de pasta foi implementado para %AppData%, e o local foi redirecionado (normalmente para um local de rede).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Diretório VFS no pacote</th>
<th align="left">Local mapeado do armazenamento de backing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProgramFilesX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</p></td>
</tr>
<tr class="even">
<td align="left"><p>SystemX86</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>appv_ROOT</p></td>
<td align="left"><p>C:\users\jsmith\AppData &lt; strong &gt; Local </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \appv_ROOT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AppData</p></td>
<td align="left"><p><strong>\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</p></td>
</tr>
</tbody>
</table>

 

 

O driver VFS cliente do App-V atual não pode gravar em locais de rede, portanto, o Cliente App-V detecta a presença de redirecionamento de pasta e copia os dados na unidade local durante a publicação e quando o ambiente virtual é iniciado. Depois que o usuário fecha o aplicativo App-V e o Cliente App-V fecha o ambiente virtual, o armazenamento local do VFS AppData é copiado de volta para a rede, habilitando o roaming para máquinas adicionais, onde o processo será repetido. As etapas detalhadas dos processos são:

1.  Durante a publicação ou a inicialização do ambiente virtual, o Cliente App-V detecta o local do diretório AppData.

2.  Se o caminho appData de roaming for local ou ino AppData\\Roaming for mapeado, nada acontecerá.

3.  Se o caminho AppData de roaming não for local, o diretório VFS AppData será mapeado para o diretório appData local.

Esse processo resolve o problema de um %AppData% não local que não é suportado pelo driver VFS do cliente App-V. No entanto, os dados armazenados nesse novo local não são roamed com redirecionamento de pasta. Todas as alterações durante a execução do aplicativo ocorrem no local appData local e devem ser copiadas para o local redirecionado. As etapas detalhadas deste processo são:

1.  O aplicativo App-V é desligado, o que desliga o ambiente virtual.

2.  O cache local do local appData em roaming é compactado e armazenado em um arquivo ZIP.

3.  Um timestamp no final do processo de empacotamento ZIP é usado para nomear o arquivo.

4.  O timestamp é registrado no Registro: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID \\AppDataTime como o último data/hora &gt; conhecido appData.

5.  O processo de redirecionamento de pasta é chamado para avaliar e iniciar o arquivo ZIP carregado no diretório AppData móveis.

O timestamp é usado para determinar um cenário de "último escritor vence" se houver um conflito e é usado para otimizar o download dos dados quando o aplicativo App-V é publicado ou o ambiente virtual é iniciado. O redirecionamento de pastas disponibiliza os dados de quaisquer outros clientes cobertos pela política de suporte e iniciará o processo de armazenamento dos dados AppData\\Roaming para o local local appData no cliente. Os processos detalhados são:

1.  O usuário inicia o ambiente virtual iniciando um aplicativo.

2.  O ambiente virtual do aplicativo verifica o arquivo ZIP com carimbo de data/hora mais recente, se presente.

3.  O Registro é verificado para o último data/hora carregado conhecido, se presente.

4.  O arquivo ZIP mais recente é baixado, a menos que o último data/hora de carregamento conhecido local seja maior ou igual ao data/hora do arquivo ZIP.

5.  Se o último data/hora de carregamento conhecido local for anterior ao arquivo ZIP mais recente no local do AppData em roaming, o arquivo ZIP será extraído para o diretório temporário local no perfil do usuário.

6.  Depois que o arquivo ZIP é extraído com êxito, o cache local do diretório AppData em roaming é renomeado e os novos dados são movidos para o local.

7.  O diretório renomeado é excluído e o aplicativo é aberto com os dados appData móveis mais recentemente salvos.

Isso conclui o roaming bem-sucedido das configurações do aplicativo presentes em AppData\\Roaming locations. A única outra condição que deve ser abordada é uma operação de reparo de pacote. Os detalhes do processo são:

1.  Durante o reparo, detecte se o caminho para o diretório AppData móveis do usuário não é local.

2.  Mapeie os destinos de caminho de AppData móveis não locais são recriados os locais de roaming e appData locais esperados.

3.  Exclua o data/hora armazenado no Registro, se presente.

Esse processo irá re-criar os locais locais e de rede para AppData e remover o registro do registro do data/hora.

## <a name="app-v-client-application-lifecycle-management"></a><a href="" id="bkmk-clt-app-lifecycle"></a>Gerenciamento do ciclo de vida do aplicativo cliente app-V


Em uma Infraestrutura Completa do App-V, depois que os aplicativos são sequenciados, eles são gerenciados e publicados para usuários ou computadores por meio dos servidores de Gerenciamento e Publicação do App-V. Esta seção detalha as operações que ocorrem durante as operações comuns do ciclo de vida do aplicativo App-V (Adicionar, publicar, iniciar, atualizar e remover) e os locais de arquivo e registro que são alterados e modificados da perspectiva do cliente App-V. As operações do Cliente app-V são executadas como uma série de comandos do PowerShell iniciados no computador que executa o Cliente App-V.

Este documento se concentra nas soluções de Infraestrutura Completa do App-V. Para obter informações específicas sobre a Integração do App-V com o Configuration Manager 2012, visite: <https://go.microsoft.com/fwlink/?LinkId=392773> .

As tarefas de ciclo de vida do aplicativo App-V são disparadas no logon do usuário (padrão), na inicialização do computador ou como operações em segundo plano. As configurações para as operações do Cliente App-V, incluindo Servidores de Publicação, intervalos de atualização, habilitação de script de pacote e outras, são configuradas durante a instalação do cliente ou pós-instalação com comandos do PowerShell. Consulte a seção Como implantar o cliente no TechNet em: Como implantar o cliente [App-V](how-to-deploy-the-app-v-client-gb18030.md) ou usar o PowerShell:

```powershell
get-command *appv*
```

### <a name="publishing-refresh"></a>Atualização de publicação

O processo de atualização de publicação é composto por várias operações menores que são executadas no Cliente App-V. Como o App-V é uma tecnologia de virtualização de aplicativos e não uma tecnologia de agendamento de tarefas, o agendador de tarefas do Windows é usado para habilitar o processo no logon do usuário, na inicialização do computador e em intervalos agendados. A configuração do cliente durante a instalação listada acima é o método preferencial ao distribuir o cliente para um grande grupo de computadores com as configurações corretas. Essas configurações de cliente podem ser configuradas com os seguintes cmdlets do PowerShell:

-   **Add-AppVPublishingServer:** Configura o cliente com um Servidor de Publicação do App-V que fornece pacotes do App-V.

-   **Set-AppVPublishingServer:** Modifica as configurações atuais do Servidor de Publicação do App-V.

-   **Set-AppVClientConfiguration:** Modifica as configurações de atualidades do Cliente App-V.

-   **Sync-AppVPublishingServer:** Inicia um processo de Atualização de Publicação do App-V manualmente. Isso também é usado nas tarefas agendadas criadas durante a configuração do servidor de publicação.

O foco das seções a seguir é detalhar as operações que ocorrem durante diferentes fases de uma Atualização de Publicação do App-V. Os tópicos incluem:

-   Adicionando um pacote do App-V

-   Publicar um pacote do App-V

### <a name="adding-an-app-v-package"></a>Adicionando um pacote do App-V

Adicionar um pacote app-V ao cliente é a primeira etapa do processo de atualização de publicação. O resultado final é o mesmo que o cmdlet no PowerShell, exceto durante o processo de adicionar atualização de publicação, o servidor de publicação configurado é contatado e passa uma lista de alto nível de aplicativos de volta para o cliente para obter informações mais detalhadas e não uma única operação de complemento de `Add-AppVClientPackage` pacote. O processo continua configurando o cliente para adições ou atualizações de pacote ou grupo de conexão e, em seguida, acessa o arquivo appv. Em seguida, o conteúdo do arquivo appv é expandido e colocado no sistema operacional local nos locais apropriados. A seguir está um fluxo de trabalho detalhado do processo, supondo que o pacote está configurado para Streaming de Falhas.

**Como adicionar um pacote do App-V**

1.  Iniciação manual por meio do PowerShell ou iniciação da Sequência de Tarefas do processo de Atualização de Publicação.

    1.  O Cliente App-V faz uma conexão HTTP e solicita uma lista de aplicativos com base no destino. O processo de atualização de publicação dá suporte a máquinas de destino ou usuários.

    2.  O Servidor de Publicação do App-V usa a identidade do destino, usuário ou máquina de inicialização e consulta o banco de dados para uma lista de aplicativos intitulados. A lista de aplicativos é fornecida como uma resposta XML, que o cliente usa para enviar solicitações adicionais ao servidor para obter mais informações por pacote.

2.  O Agente de Publicação no Cliente App-V executa todas as ações abaixo serializadas.

    Avalie todos os grupos de conexão que não sejam publicados ou desabilitados, pois as atualizações de versão do pacote que fazem parte do grupo de conexão não podem ser processadas.

3.  Configure os pacotes identificando uma operação Adicionar ou Atualizar.

    1.  O Cliente App-V utiliza a API AppX Windows e acessa o arquivo appv do servidor de publicação.

    2.  O arquivo de pacote é aberto e os AppXManifest.xml e StreamMap.xml são baixados para o Package Store.

    3.  Fluxo completo de dados de bloqueio de publicação definidos no StreamMap.xml. Armazena os dados de bloqueio de publicação no Package Store\\PkgGUID\\VerGUID\\Root.

        -   Ícones: Destinos de pontos de extensão.

        -   Headers Executáveis Portáteis (Headers PE): destinos de pontos de extensão que contêm as informações básicas sobre a necessidade de imagem no disco, acessados diretamente ou por meio de tipos de arquivo.

        -   Scripts: Baixe o diretório de scripts para uso em todo o processo de publicação.

    4.  Preencher o armazenamento de pacotes:

        1.  Crie arquivos esparsos no disco que representam o pacote extraído para todos os diretórios listados.

        2.  Arquivos e diretórios de nível superior em estágio raiz.

        3.  Todos os outros arquivos são criados quando o diretório é listado como esparso no disco e transmitido sob demanda.

    5.  Crie as entradas do catálogo de máquinas. Crie o Manifest.xml e DeploymentConfiguration.xml dos arquivos do pacote (se nenhum arquivo DeploymentConfiguration.xml no pacote em que um espaço reservado for criado).

    6.  Criar o local do armazenamento de pacotes no HKLM do Registro\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog

    7.  Crie o arquivo Registry.dat do armazenamento de pacotes para %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat

    8.  Registrar o pacote com o HKLM do Driver do Modo Kernel do App-V\\Microsoft\\Software\\AppV\\MAV

    9.  Invocar scripts do arquivo AppxManifest.xml ou DeploymentConfig.xml tempo para Adicionar pacote.

4.  Configure Os Grupos de Conexão adicionando e habilitando ou desabilitando.

5.  Remova objetos que não são publicados no destino (usuário ou máquina).

    **Observação**  
    Isso não executará uma exclusão de pacote, mas removerá pontos de integração para o destino específico (usuário ou máquina) e removerá arquivos de catálogo de usuários (arquivos de catálogo de máquina para publicação global).

     

6.  Invocar a montagem de carga em segundo plano com base na configuração do cliente.

7.  Pacotes que já têm informações de publicação para o computador ou usuário são imediatamente restaurados.

    **Observação**  
    Essa condição ocorre como um produto de remoção sem a des publicação com a adição em segundo plano do pacote.

     

Isso conclui um complemento de pacote do App-V do processo de atualização de publicação. A próxima etapa é publicar o pacote para o destino específico (máquina ou usuário).

![package add file and Registry data.](images/packageaddfileandregistrydata.png)

### <a name="publishing-an-app-v-package"></a>Publicar um pacote do App-V

Durante a operação Atualização de Publicação, a operação de publicação específica (Publish-AppVClientPackage) adiciona entradas ao catálogo de usuários, mapeia o direito ao usuário, identifica o armazenamento local e conclui concluindo todas as etapas de integração. A seguir estão as etapas detalhadas.

**Como publicar e o pacote do App-V**

1.  Entradas de pacote são adicionadas ao catálogo de usuários

    1.  Pacotes direcionados ao usuário: os UserDeploymentConfiguration.xml e UserManifest.xml são colocados no computador no Catálogo de Usuários

    2.  Pacotes direcionados para máquina (globais): o UserDeploymentConfiguration.xml é colocado no Catálogo de Máquinas

2.  Registre o pacote com o driver de modo kernel para o usuário em HKLM\\Software\\Microsoft\\AppV\\MAV

3.  Executar tarefas de integração.

    1.  Criar pontos de extensão.

    2.  Armazene informações de backup no registro e no perfil de roaming do usuário (Backups de atalho).

        **Observação**  
        Isso permite restaurar pontos de extensão se o pacote não for publicado.

         

    3.  Execute scripts direcionados para o tempo de publicação.

Publicar um Pacote do App-V que faz parte de um Grupo de Conexão é muito semelhante ao processo acima. Para grupos de conexão, o caminho que armazena as informações de catálogo específicas inclui PackageGroups como filho do Diretório de Catálogos. Revise as informações do catálogo do computador e dos usuários acima para obter detalhes.

![package add file and Registry data - global.](images/packageaddfileandregistrydata-global.png)

### <a name="application-launch"></a>Início do aplicativo

Após o processo de Atualização de Publicação, o usuário inicia e, posteriormente, reaciona um aplicativo App-V. O processo é muito simples e otimizado para ser lançado rapidamente com um mínimo de tráfego de rede. O Cliente App-V verifica o caminho para o catálogo de usuários para arquivos criados durante a publicação. Depois que os direitos para iniciar o pacote são estabelecidos, o Cliente App-V cria um ambiente virtual, começa a transmitir todos os dados necessários e aplica os arquivos de configuração de manifesto e implantação apropriados durante a criação do ambiente virtual. Com o ambiente virtual criado e configurado para o pacote e aplicativo específicos, o aplicativo é iniciado.

**Como iniciar aplicativos App-V**

1.  O usuário inicia o aplicativo clicando em um atalho ou invocação de tipo de arquivo.

2.  O Cliente App-V verifica a existência no Catálogo de Usuários para os seguintes arquivos

    -   UserDeploymentConfiguration.xml

    -   UserManifest.xml

3.  Se os arquivos estão presentes, o aplicativo tem direito a esse usuário específico e o aplicativo iniciará o processo de início. Não há tráfego de rede neste ponto.

4.  Em seguida, o Cliente App-V verifica se o caminho do pacote registrado para o serviço cliente App-V é encontrado no Registro.

5.  Ao encontrar o caminho para o armazenamento de pacotes, o ambiente virtual é criado. Se esse for o primeiro lançamento, o Bloco de Recursos Principais será baixado se estiver presente.

6.  Depois de baixar, o serviço cliente App-V consome os arquivos de configuração de manifesto e implantação para configurar o ambiente virtual e todos os subsistemas do App-V são carregados.

7.  O Aplicativo é lançado. Para quaisquer arquivos ausentes no armazenamento de pacotes (arquivos esparsos), o App-V transmitirá falhas nos arquivos conforme necessário.

    ![package add file and Registry data - stream.](images/packageaddfileandregistrydata-stream.png)

### <a name="upgrading-an-app-v-package"></a>Atualizando um pacote do App-V

O processo de atualização de pacote do App-V 5 difere das versões mais antigas do App-V. O App-V dá suporte a várias versões do mesmo pacote em um computador com direito a usuários diferentes. As versões do pacote podem ser adicionadas a qualquer momento à medida que o armazenamento de pacotes e catálogos são atualizados com os novos recursos. O único processo específico para a adição de novos recursos de versão é a otimização de armazenamento. Durante uma atualização, apenas os novos arquivos são adicionados ao novo local do armazenamento de versão e os links rígidos são criados para arquivos inalterados. Isso reduz o armazenamento geral apresentando apenas o arquivo em um local de disco e projetando-o em todas as pastas com uma entrada de local de arquivo no disco. Os detalhes específicos da atualização de um Pacote do App-V são:

**Como atualizar um pacote do App-V**

1.  O Cliente App-V executa uma Atualização de Publicação e descobre uma versão mais recente de um Pacote app-V.

2.  Entradas de pacote são adicionadas ao catálogo apropriado para a nova versão

    1.  Pacotes direcionados ao usuário: os UserDeploymentConfiguration.xml e UserManifest.xml são colocados no computador no catálogo de usuários em appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

    2.  Pacotes direcionados a máquina (global): o UserDeploymentConfiguration.xml é colocado no catálogo de máquinas em %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID

3.  Registre o pacote com o driver de modo kernel para o usuário em HKLM\\Software\\Microsoft\\AppV\\MAV

4.  Executar tarefas de integração.

    -   Integre pontos de extensão (EP) dos arquivos Manifesto e Configuração Dinâmica.

    1.  Os dados ep baseados em arquivo são armazenados na pasta AppData usando Pontos de Junção do armazenamento do pacote.

    2.  Os EPs da versão 1 já existem quando uma nova versão fica disponível.

    3.  Os pontos de extensão são alternados para o local da Versão 2 em catálogos de computador ou de usuário para quaisquer pontos de extensão mais novos ou atualizados.

5.  Execute scripts direcionados para o tempo de publicação.

6.  Instalar assemblies lado a lado conforme necessário.

### <a name="upgrading-an-in-use-app-v-package"></a>Atualizando um pacote do App-V em uso

**A partir do App-V 5 SP2**: Se você tentar atualizar um pacote que está em uso por um usuário final, a tarefa de atualização será colocada em um estado pendente. A atualização será executado posteriormente, de acordo com as seguintes regras:

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
<td align="left"><p>Tarefa baseada no usuário, por exemplo, publicar um pacote para um usuário</p></td>
<td align="left"><p>A tarefa pendente será executada depois que o usuário fazer logo off e fazer logo logs novamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tarefa baseada globalmente, por exemplo, habilitando um grupo de conexão globalmente</p></td>
<td align="left"><p>A tarefa pendente será executada quando o computador for desligado e reiniciado.</p></td>
</tr>
</tbody>
</table>

 

Quando uma tarefa é colocada em um estado pendente, o cliente App-V também gera uma chave do Registro para a tarefa pendente, da seguinte forma:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa baseada no usuário ou globalmente</th>
<th align="left">Onde a chave do Registro é gerada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tarefas baseadas no usuário</p></td>
<td align="left"><p>KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tarefas baseadas globalmente</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</p></td>
</tr>
</tbody>
</table>

 

As seguintes operações devem ser concluídas antes que os usuários possam usar a versão mais recente do pacote:

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
<td align="left"><p>Essa tarefa é específica do computador e você pode realificá-la a qualquer momento, concluindo as etapas na seção Adicionar pacote acima.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publicar o pacote</p></td>
<td align="left"><p>Consulte a seção Publicação de Pacote acima para ver as etapas. Esse processo exige que você atualize pontos de extensão no sistema. Os usuários finais não podem estar usando o aplicativo ao concluir essa tarefa.</p></td>
</tr>
</tbody>
</table>

 

Use os cenários de exemplo a seguir como um guia para atualizar pacotes.

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
<td align="left"><p>Nenhum dos seguintes componentes do pacote pode estar em uso: aplicativo virtual, servidor COM ou extensões de shell.</p>
<p>O administrador publica uma versão mais recente do pacote e a atualização funciona na próxima vez que um componente ou aplicativo dentro do pacote é lançado. A nova versão do pacote é transmitida e executado. Nada mudou nesse cenário no App-V 5 SP2 de versões anteriores do App-V 5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>O pacote do App-V está em uso quando o administrador publica uma versão mais recente do pacote</p></td>
<td align="left"><p>A operação de atualização é definida como pendente pelo Cliente App-V, o que significa que ela está em fila e executada posteriormente quando o pacote não está em uso.</p>
<p>Se o aplicativo de pacote estiver em uso, o usuário desligará o aplicativo virtual, após o qual a atualização poderá ocorrer.</p>
<p>Se o pacote tiver extensões de shell (Office 2013), que são carregadas permanentemente pelo Windows Explorer, o usuário não poderá ser conectado. Os usuários devem fazer logoff e o log de volta para iniciar a atualização do pacote app-V.</p></td>
</tr>
</tbody>
</table>

 

### <a name="global-vs-user-publishing"></a>Publicação global versus usuário

Os Pacotes do App-V podem ser publicados de duas maneiras; Usuário que dá direito a um pacote do App-V a um usuário ou grupo específico de usuários e Global que dá direito ao pacote app-V para todo o computador para todos os usuários do computador. Depois que uma atualização de pacote tiver sido reprisada e o pacote do App-V não for usado, considere os dois tipos de publicação:

-   **Publicado globalmente:** o aplicativo é publicado em um computador; todos os usuários nesse computador podem usá-lo. A atualização acontecerá quando o Serviço de Cliente do App-V for iniciado, o que efetivamente significa uma reinicialização do computador.

-   **Usuário publicado**: o aplicativo é publicado para um usuário. Se houver vários usuários no computador, o aplicativo poderá ser publicado em um subconjunto dos usuários. A atualização acontecerá quando o usuário entrar ou quando for publicado novamente (periodicamente, atualização e avaliação da Política de ConfigMgr, ou uma publicação/atualização periódica do App-V ou explicitamente por meio de comandos do PowerShell).

### <a name="removing-an-app-v-package"></a>Removendo um pacote do App-V

Remover aplicativos App-V em uma Infraestrutura Completa é uma operação não publicada e não executa uma remoção de pacote. O processo é igual ao processo de publicação acima, mas, em vez de adicionar o processo de remoção, reverte as alterações feitas nos Pacotes do App-V.

### <a name="repairing-an-app-v-package"></a>Reparar um pacote do App-V

A operação de reparo é muito simples, mas pode afetar muitos locais no computador. Os locais anteriormente mencionados copy on Write (VACA) são removidos e os pontos de extensão são des integrados e, em seguida, re-integrados. Revise os locais de posicionamento de dados DE VACA revendo onde estão registrados no Registro. Essa operação é feita automaticamente e não há outro controle administrativo além de iniciar uma operação de Reparo do Console cliente app-V ou por meio do PowerShell (Repair-AppVClientPackage).

## <a name="integration-of-app-v-packages"></a><a href="" id="bkmk-integr-appv-pkgs"></a>Integração de pacotes do App-V


O Cliente do App-V e a arquitetura de pacote fornece integração específica com o sistema operacional local durante a adição e publicação de pacotes. Três arquivos definem os pontos de integração ou extensão de um Pacote app-V:

-   AppXManifest.xml: Armazenado dentro do pacote com cópias de fallback armazenadas no armazenamento de pacotes e no perfil do usuário. Contém as opções criadas durante o processo de sequenciamento.

-   DeploymentConfig.xml: fornece informações de configuração de pontos de extensão de integração baseados no computador e no usuário.

-   UserConfig.xml: um subconjunto do Deploymentconfig.xml que fornece apenas configurações baseadas no usuário e direciona somente pontos de extensão baseados no usuário.

### <a name="rules-of-integration"></a>Regras de integração

Quando os aplicativos App-V são publicados em um computador com o Cliente App-V, algumas ações específicas ocorrem conforme descrito na lista abaixo:

-   Publicação Global: os atalhos são armazenados no local de perfil Todos os Usuários e outros pontos de extensão são armazenados no Registro no hive HKLM.

-   Publicação do usuário: os atalhos são armazenados no perfil de conta de usuário atual e outros pontos de extensão são armazenados no Registro no hive HKCU.

-   Backup e Restauração: dados e registro de aplicativos nativos existentes (como registros FTA) são backups durante a publicação.

    1.  Os pacotes do App-V são propriedade com base no último pacote integrado em que a propriedade é passada para o aplicativo App-V mais recente publicado.

    2.  Transferências de propriedade de um pacote do App-V para outro quando o pacote do App-V proprietário é não publicado. Isso não iniciará uma restauração dos dados ou do Registro.

    3.  Restaure os dados de backup quando o último pacote for não publicado ou removido por ponto de extensão.

### <a name="extension-points"></a>Pontos de extensão

Os arquivos de publicação do App-V (manifesto e configuração dinâmica) fornecem vários pontos de extensão que permitem que o aplicativo se integre ao sistema operacional local. Esses pontos de extensão executam tarefas típicas de instalação do aplicativo, como colocar atalhos, criar associações de tipos de arquivo e registrar componentes. Como são aplicativos virtualizados que não são instalados da mesma maneira que um aplicativo tradicional, há algumas diferenças. Veja a seguir uma lista de pontos de extensão abordados nesta seção:

-   Atalhos

-   Associações de tipo de arquivo

-   Extensões do Shell

-   COM

-   Clientes de software

-   Recursos do aplicativo

-   Manipulador de protocolo URL

-   AppPath

-   Aplicativo Virtual

### <a name="shortcuts"></a>Atalhos

O atalho é um dos elementos básicos de integração com o sistema operacional e é a interface para o início direto do usuário de um aplicativo App-V. Durante a publicação e a não publicação de aplicativos App-V.

No manifesto do pacote e nos arquivos XML de configuração dinâmica, o caminho para um executável de aplicativo específico pode ser encontrado em uma seção semelhante à seguinte:

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

Conforme mencionado anteriormente, os atalhos do App-V são colocados por padrão no perfil do usuário com base na operação de atualização. A atualização global coloca atalhos no perfil Todos os Usuários e a atualização do usuário os armazena no perfil do usuário específico. O executável real é armazenado no Package Store. O local do arquivo ICO é um local tokenizado no pacote app-V.

### <a name="file-type-associations"></a>Associações de tipo de arquivo

O Cliente App-V gerencia as Associações de Tipo de Arquivo do sistema operacional local durante a publicação, o que permite que os usuários usem invocações de tipo de arquivo ou abram um arquivo com uma extensão especificamente registrada (.docx) para iniciar um aplicativo App-V. Associações de tipo de arquivo estão presentes nos arquivos de manifesto e configuração dinâmica, conforme representado no exemplo abaixo:

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

**Observação**  
Neste exemplo:

-   `<Name>.xdp</Name>` é a extensão

-   `<Name>AcroExch.XDPDoc</Name>` é o valor ProgId (que aponta para o ProgId adjacente)

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` é a linha de comando, que aponta para o executável do aplicativo

 

### <a name="shell-extensions"></a>Extensões de shell

As extensões do Shell são inseridas no pacote automaticamente durante o processo de sequenciamento. Quando o pacote é publicado globalmente, a extensão do shell fornece aos usuários a mesma funcionalidade que se o aplicativo foi instalado localmente. O aplicativo não requer configuração adicional no cliente para habilitar a funcionalidade de extensão do shell.

**Requisitos para usar extensões de shell:**

-   Os pacotes que contêm extensões de shell incorporados devem ser publicados globalmente.

-   A "bitness" do aplicativo, sequencer e cliente App-V deve corresponder, ou as extensões de shell não funcionarão. Por exemplo:

    -   A versão do aplicativo é de 64 bits.

    -   O Sequencer está sendo executado em um computador de 64 bits.

    -   O pacote está sendo entregue a um computador cliente app-V de 64 bits.

A tabela a seguir exibe as extensões de shell com suporte.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Manipulador</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Manipulador de menus de contexto</p></td>
<td align="left"><p>Adiciona itens de menu ao menu de contexto. Ele é chamado antes que o menu de contexto seja exibido.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de arrastar e soltar</p></td>
<td align="left"><p>Controla a ação ao clicar com o botão direito do mouse em arrastar e soltar e modifica o menu de contexto que aparece.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de destino de soltar</p></td>
<td align="left"><p>Controla a ação depois que um objeto de dados é arrastado e descartado sobre um destino de soltar, como um arquivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de objetos de dados</p></td>
<td align="left"><p>Controla a ação depois que um arquivo é copiado para a área de transferência ou arrastado e descartado sobre um destino de soltar. Ele pode fornecer formatos de área de transferência adicionais para o destino de entrega.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de planilhas de propriedades</p></td>
<td align="left"><p>Substitui ou adiciona páginas à caixa de diálogo folha de propriedades de um objeto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de dicas de informações</p></td>
<td align="left"><p>Permite recuperar sinalizadores e informações de infotipagem para um item e exibi-lo dentro de uma dica de ferramenta pop-up no mouse- hover.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de colunas</p></td>
<td align="left"><p>Permite criar e exibir colunas personalizadas no Windows <em> de detalhes do </em> Explorer. Ele pode ser usado para estender a classificação e o agrupamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de visualização</p></td>
<td align="left"><p>Permite uma visualização de um arquivo a ser exibido no painel de visualização Windows Explorer.</p></td>
</tr>
</tbody>
</table>

 

### <a name="com"></a>COM

O Cliente App-V dá suporte a aplicativos de publicação com suporte para integração e virtualização com COM. A integração com permite que o Cliente App-V registre objetos COM no sistema operacional local e virtualização dos objetos. Para os fins deste documento, a integração de objetos COM requer detalhes adicionais.

O App-V dá suporte ao registro de objetos COM do pacote para o sistema operacional local com dois tipos de processo: fora de processo e em processo. O registro de objetos COM é realizado com uma ou uma combinação de vários modos de operação para um pacote específico do App-V que inclui off, Isolated e Integrated. O modo integrado é configurado para o tipo fora do processo ou no processo. A configuração de modos e tipos COM é realizada com arquivos de configuração dinâmicos (deploymentconfig.xml ou userconfig.xml).

Os detalhes sobre a integração com o App-V estão disponíveis em: <https://go.microsoft.com/fwlink/?LinkId=392834> .

### <a name="software-clients-and-application-capabilities"></a>Clientes de software e recursos de aplicativos

O App-V oferece suporte a clientes de software específicos e pontos de extensão de recursos de aplicativos que permitem que aplicativos virtualizados sejam registrados com o cliente de software do sistema operacional. Isso permite que os usuários selecionem programas padrão para operações como email, mensagens instantâneas e media player. Essa operação é executada no painel de controle com o Set Program Access and Computer Defaults e configurada durante o sequenciamento nos arquivos de manifesto ou configuração dinâmica. Os recursos do aplicativo só são suportados quando os aplicativos App-V são publicados globalmente.

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

**Observação**  
Neste exemplo:

-   `<ClientConfiguration EmailEnabled="true" />` é a configuração geral de Clientes de Software para integrar clientes de email

-   `<EMail MakeDefault="true">` é o sinalizador para definir um determinado cliente de Email como o cliente de Email padrão

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` é o registro DLL MAPI

 

### <a name="url-protocol-handler"></a>Manipulador de protocolo URL

Os aplicativos nem sempre são chamados especificamente de aplicativos virtualizados que usam invocação de tipo de arquivo. Por exemplo, em um aplicativo que dá suporte à incorporação de um mailto: link dentro de um documento ou página da Web, o usuário clica em um link mailto: e espera obter seu cliente de email registrado. O App-V dá suporte a manipuladores de Protocolo de URL que podem ser registrados por pacote com o sistema operacional local. Durante a sequenciamento, os manipuladores de protocolo URL são adicionados automaticamente ao pacote.

Para situações em que há mais de um aplicativo que poderia registrar o manipulador de Protocolo de URL específico, os arquivos de configuração dinâmica podem ser usados para modificar o comportamento e suprimir ou desabilitar esse recurso para um aplicativo que não deve ser o aplicativo principal lançado.

### <a name="apppath"></a>AppPath

O ponto de extensão do AppPath dá suporte à chamada de aplicativos App-V diretamente do sistema operacional. Isso normalmente é feito a partir da Tela De execução ou início, dependendo do sistema operacional, que permite que os administradores forneçam acesso a aplicativos App-V a partir de comandos ou scripts do sistema operacional sem chamar o caminho específico para o executável. Portanto, evita modificar a variável do ambiente de caminho do sistema em todos os sistemas, conforme é feito durante a publicação.

O ponto de extensão do AppPath é configurado no manifesto ou nos arquivos de configuração dinâmica e é armazenado no Registro no computador local durante a publicação para o usuário. Para obter informações adicionais sobre a revisão do AppPath: <https://go.microsoft.com/fwlink/?LinkId=392835> .

### <a name="virtual-application"></a>Aplicativo virtual

Esse subsistema fornece uma lista de aplicativos capturados durante o sequenciamento, que geralmente é consumido por outros componentes do App-V. A integração de pontos de extensão pertencentes a um aplicativo específico pode ser desabilitada usando arquivos de configuração dinâmica. Por exemplo, se um pacote contiver dois aplicativos, é possível desabilitar todos os pontos de extensão pertencentes a um aplicativo, para permitir apenas a integração de pontos de extensão de outro aplicativo.

### <a name="extension-point-rules"></a>Regras de ponto de extensão

Os pontos de extensão descritos acima são integrados ao sistema operacional com base em como os pacotes foram publicados. A publicação global coloca pontos de extensão em locais de máquina pública, onde a publicação do usuário coloca pontos de extensão em locais de usuários. Por exemplo, um atalho criado na área de trabalho e publicado globalmente resultará nos dados de arquivo para o atalho (%Public%\\Desktop) e os dados do Registro (HKLM\\Software\\Classes). O mesmo atalho teria dados de arquivo (%UserProfile%\\Desktop) e dados do Registro (HKCU\\Software\\Classes).

Os pontos de extensão não são todos publicados da mesma maneira, onde alguns pontos de extensão exigirão publicação global e outros exigem sequenciamento no sistema operacional e na arquitetura específicos onde são entregues. Abaixo está uma tabela que descreve essas duas regras principais.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Extensão Virtual</th>
<th align="left">Requer sequenciamento do sistema operacional de destino</th>
<th align="left">Requer Publicação Global</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Atalho</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Associação de Tipo de Arquivo</p></td>
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
<td align="left"><p>Cliente de Software</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Recursos do aplicativo</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de menus de contexto</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de arrastar e soltar</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de objetos de dados</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de Planilhas de Propriedades</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Manipulador de dicas de informações</p></td>
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
<td align="left"><p>Objeto Auxiliar do Navegador</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
<tr class="even">
<td align="left"><p>Objeto Active X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
</tr>
</tbody>
</table>

 

## <a name="dynamic-configuration-processing"></a><a href="" id="bkmk-dynamic-config"></a>Processamento de configuração dinâmica


Implantar pacotes do App-V em um computador ou usuário é muito simples. No entanto, à medida que as organizações implantam aplicativos AppV em linhas comerciais e limites geográficos e políticos, a capacidade de sequenciar um aplicativo uma vez com um conjunto de configurações se torna impossível. O App-V foi projetado para esse cenário, pois captura configurações e configurações específicas durante o sequenciamento no arquivo Manifesto, mas também dá suporte à modificação com arquivos de Configuração Dinâmica.

A configuração dinâmica do App-V permite especificar uma política para um pacote no nível do computador ou no nível do usuário. Os arquivos de Configuração Dinâmica permitem que os engenheiros de sequenciamento modifiquem a configuração de um pacote, pós-sequenciamento, para atender às necessidades de grupos individuais de usuários ou máquinas. Em algumas instâncias, pode ser necessário fazer modificações no aplicativo para fornecer a funcionalidade adequada no ambiente do App-V. Por exemplo, pode ser necessário fazer modificações nos arquivos \_\*config.xml para permitir que determinadas ações sejam executadas em um momento especificado durante a execução do aplicativo, como desabilitar uma extensão mailto para impedir que um aplicativo virtualizado sobrescreva essa extensão de outro aplicativo.

Os Pacotes app-V contêm o arquivo De manifesto dentro do arquivo de pacote do appv, que representa as operações de sequenciamento e é a política de escolha, a menos que os arquivos de Configuração Dinâmica sejam atribuídos a um pacote específico. Após a sequenciamento, os arquivos de Configuração Dinâmica podem ser modificados para permitir a publicação de um aplicativo em diferentes áreas de trabalho ou usuários com pontos de extensão diferentes. Os dois Arquivos de Configuração Dinâmica são os arquivos DDC (Dynamic Deployment Configuration) e Dynamic User Configuration (DUC). Esta seção se concentra na combinação dos arquivos de manifesto e configuração dinâmica.

### <a name="example-for-dynamic-configuration-files"></a>Exemplo para arquivos de configuração dinâmica

O exemplo a seguir mostra a combinação dos arquivos Manifesto, Configuração de Implantação e Configuração do Usuário após a publicação e durante a operação normal. Esses exemplos são exemplos abreviados de cada um dos arquivos. A finalidade é mostrar a combinação apenas dos arquivos e não ser uma descrição completa das categorias específicas disponíveis em cada um dos arquivos. Para obter mais informações, revise o Guia de Sequenciamento do App-V 5 em: <https://go.microsoft.com/fwlink/?LinkID=269810>

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

**Configuração de Implantação**

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

**Configuração do Usuário**

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

## <a name="side-by-side-assemblies"></a><a href="" id="bkmk-sidebyside-assemblies"></a>Assemblies lado a lado


O App-V dá suporte ao empacotamento automático de assemblies lado a lado (SxS) durante a sequenciamento e a implantação no cliente durante a publicação do aplicativo virtual. O App-V 5 SP2 dá suporte à captura de assemblies SxS durante a sequenciamento para assemblies não presentes no computador de sequenciamento. E para assemblies que consistem em Visual C++ (Versão 8 e mais recente) e/ou MSXML tempo de executar, o Sequencer detectará e capturará automaticamente essas dependências, mesmo que não foram instaladas durante o monitoramento. O recurso Assemblies Lado a Lado remove as limitações das versões anteriores do App-V, onde o App-V Sequencer não captura assemblies já presentes na estação de trabalho de sequenciamento e desempacota os assemblies que se limitam a uma versão de bits por pacote. Esse comportamento resultou na implantação de aplicativos App-V para clientes que não estavam nos assemblies SxS necessários, causando falhas de início do aplicativo. Isso forçava o processo de empacotamento a documentar e, em seguida, garantir que todos os assemblies necessários para pacotes fossem instalados localmente no sistema operacional cliente do usuário para garantir o suporte para os aplicativos virtuais. Com base no número de assemblies e na falta de documentação do aplicativo para as dependências necessárias, essa tarefa era um desafio de gerenciamento e implementação.

O suporte ao Assembly Lado a Lado no App-V tem os seguintes recursos.

-   Capturas automáticas do assembly SxS durante a Sequenciamento, independentemente de o assembly já ter sido instalado na estação de trabalho de sequenciamento.

-   O Cliente App-V instala automaticamente os assemblies SxS necessários ao computador cliente no momento da publicação quando eles não estão presentes.

-   O Sequencer relata a dependência de tempo de executar VC no mecanismo de relatório do Sequencer.

-   O Sequencer permite optar por não empacotar os assemblies que já estão instalados no Sequencer, suportando cenários em que os assemblies foram instalados anteriormente nos computadores de destino.

### <a name="automatic-publishing-of-sxs-assemblies"></a>Publicação automática de assemblies SxS

Durante a publicação de um pacote do App-V com assemblies SxS, o Cliente do App-V verificará a presença do assembly no computador. Se o assembly não existir, o cliente implantará o assembly no computador. Os pacotes que fazem parte de grupos de conexão dependerão das instalações de assembly lado a lado que fazem parte dos pacotes base, pois o grupo de conexão não contém informações sobre a instalação do assembly.

**Observação**  
A unPublishing or remove a package with an assembly does not remove the assemblies for that package.

 

## <a name="client-logging"></a><a href="" id="bkmk-client-logging"></a>Log do cliente


O cliente App-V registra informações no log de eventos Windows no formato ETW padrão. Os eventos específicos do App-V podem ser encontrados no visualizador de eventos, em Logs de Aplicativos e Serviços\\Microsoft\\AppV\\Client.

**Observação**  
No App-V 5.0 SP3, alguns logs foram consolidados e movidos para o seguinte local:

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

Para ver uma lista dos logs movidos, consulte [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

 

Há três categorias específicas de eventos registrados descritos abaixo.

**Admin**: registra eventos para configurações que estão sendo aplicadas ao Cliente App-V e contém os principais avisos e erros.

**Operacional**: registra a execução geral do App-V e o uso de componentes individuais criando um log de auditoria das operações do App-V que foram concluídas no Cliente App-V.

**Aplicativo Virtual**: registra os lançamentos de aplicativos virtuais e o uso de subsistemas de virtualização.






 

 





