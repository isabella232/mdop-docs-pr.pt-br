---
title: Sobre o App-V 5.1
description: Sobre o App-V 5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796627"
---
# Sobre o App-V 5.1


Use as seções a seguir para analisar informações sobre alterações significativas que se aplicam ao Application Virtualization (App-V) 5,1:

[Pré-requisitos de software do App-V 5,1 e configurações com suporte](#bkmk-51-prereq-configs)

[Migrando para o App-V 5,1](#bkmk-migrate-to-51)

[O que há de novo no App-V 5,1](#bkmk-whatsnew)

[Suporte do App-V para Windows 10](#bkmk-win10support)

[Alterações no console de gerenciamento do App-V](#bkmk-mgmtconsole)

[Melhorias do sequenciador](#bkmk-seqimprove)

[Melhorias no conversor de pacote](#bkmk-pkgconvimprove)

[Suporte para vários scripts em um único gatilho de evento](#bkmk-supmultscripts)

[Caminho codificado para a pasta de instalação é redirecionado para a raiz do sistema de arquivos virtual](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a>Pré-requisitos de software do App-V 5,1 e configurações com suporte


Confira os links a seguir para os pré-requisitos de software do App-V 5,1 e as configurações com suporte.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Links para pré-requisitos e configurações com suporte</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)">Pré-requisitos do App-V 5.1</a></p></td>
<td align="left"><p>Software obrigatório que você deve instalar antes de iniciar a instalação do App-V 5,1</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">Configurações com suporte ao App-V 5.1</a></p></td>
<td align="left"><p>Sistemas operacionais com suporte e requisitos de hardware para os componentes App-V Server, Sequencer e cliente</p></td>
</tr>
</tbody>
</table>



**Suporte para usar o Configuration Manager com App-V:** O App-V 5,1 dá suporte ao System Center 2012 R2 Configuration Manager SP1. Consulte [planejando a integração do App-v com o Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) para obter informações sobre como integrar seu ambiente app-v com o Configuration Manager e o Configuration Manager.

## <a href="" id="bkmk-migrate-to-51"></a>Migrando para o App-V 5,1


Use as informações a seguir para atualizar para o App-V 5,1 de versões anteriores. Para obter mais informações, confira [migrar para o App-V 5,1 de uma versão anterior](migrating-to-app-v-51-from-a-previous-version.md) .

### Antes de iniciar a atualização

Revise as seguintes informações antes de iniciar a atualização:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Itens a serem revisados antes da atualização</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Componentes para atualização, em qualquer ordem</p></td>
<td align="left"><ol>
<li><p>Servidor do App-V</p></li>
<li><p>Sequenciador</p></li>
<li><p>Cliente App-V ou serviços de área de trabalho remota do App-V (RDS)</p></li>
</ol>
<div class="alert">
<strong>Observação</strong><br/><p>Antes do App-V 5,0 SP2, a interface do usuário de gerenciamento do cliente (UI) foi fornecida com a instalação do cliente do App-V. Para instalações do App-V 5,0 SP2 (ou posterior), você pode usar a interface do usuário de gerenciamento de cliente ao baixar do <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> aplicativo de interface do usuário do cliente do Application Virtualization 5,0 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Atualizando do App-V 4. x</p></td>
<td align="left"><p>Primeiro você deve atualizar para o App-V 5,0. Você não pode atualizar diretamente do App-V 4. x para o App-V 5,1. Para obter mais informações, consulte:</p>
<ul>
<li><p>"Diferenças entre o App-V 4,6 e o App-V 5,0" em <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> sobre o app-v 5,0</a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Planejamento para a migração de uma versão anterior do App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Atualizando a partir do App-V 5,0 ou posterior</p></td>
<td align="left"><p>Você pode atualizar para o App-V 5,1 diretamente de qualquer uma das seguintes versões:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
<li><p>App-V 5,0 SP3</p></li>
</ul>
<p>Para atualizar para o App-V 5,1, siga as etapas nas seções restantes deste tópico.</p>
<p>Pacotes e grupos de conexão continuarão a funcionar com o App-V 5,1, como fazem no momento.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Etapas para atualizar a infraestrutura do App-V

Conclua as etapas a seguir para atualizar cada componente da infraestrutura do App-V para o App-V 5,1. A ordem a seguir é apenas uma sugestão; Você pode atualizar componentes em qualquer ordem.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Etapa</th>
<th align="left">Para obter mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Etapa 1: Atualize o App-V Server.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Se você não estiver usando o servidor App-V, pule esta etapa e vá para a próxima etapa.</p>
</div>
<div>

</div></td>
<td align="left"><p>Siga estas etapas: </p>
<ol>
<li><p>Siga um destes procedimentos, dependendo do método que você está usando para atualizar o banco de dados de gerenciamento e/ou banco de dados de relatórios:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método de atualização de banco de dados</th>
<th align="left">Etapa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Pule esta etapa e vá para a etapa 2, "se você estiver atualizando o App-V Server..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scripts SQL</p></td>
<td align="left"><p>Siga as etapas em <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> como implantar os bancos de dados do App-V usando scripts SQL </a> .</p></td>
</tr>
</tbody>
</table>
<li><p>Se você estiver atualizando o pacote do pacote do aplicativo App-V do App-V 5,0 SP1 3 ou posterior, conclua as etapas na seção <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> Verifique as chaves do registro após instalar o servidor App-V 5,0 SP3 </a> .</p></li>
<li><p>Siga as etapas em <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> como implantar o servidor do App-V 5,1</a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Etapa 2: Atualize o sequenciador do App-V.</p></td>
<td align="left"><p>Veja <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> como instalar o sequenciador </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Etapa 3: Atualize o cliente App-V ou o App-V RDS Client.</p></td>
<td align="left"><p>Veja <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> como implantar o cliente App-V </a> .</p></td>
</tr>
</tbody>
</table>



### Convertendo pacotes criados usando uma versão anterior do App-V

Use o utilitário conversor de pacote para atualizar pacotes de aplicativos virtuais criados usando versões do App-V antes do App-V 5,0. O conversor de pacote usa o PowerShell para converter pacotes e pode ajudar a automatizar o processo se você tiver muitos pacotes que exijam conversão.

**Observação**  
Os pacotes do App-V 5,1 são exatamente iguais aos pacotes do App-V 5,0. Não houve nenhuma alteração no formato do pacote entre as versões e, portanto, não há necessidade de converter pacotes do App-V 5,0 em pacotes do App-V 5,1.



## <a href="" id="bkmk-whatsnew"></a>O que há de novo no App-V 5,1


Estas seções destinam-se aos usuários que já estão familiarizados com o App-V e querem saber o que mudou no App-V 5,1. Se você ainda não estiver familiarizado com o App-V, comece lendo planejando o [app-v 5,1](planning-for-app-v-51.md).

### <a href="" id="bkmk-win10support"></a>Suporte do App-V para Windows 10

A tabela a seguir lista o suporte do Windows 10 para App-V. Não há suporte para o Windows 10 em versões do App-V antes do App-V 5,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">App-V 5.1</th>
<th align="left">App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cliente App-V</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente RDS do App-V</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequenciador App-V</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Não</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a>Alterações no console de gerenciamento do App-V

Esta seção compara a funcionalidade atual e anterior do console de gerenciamento do App-V.

### O Silverlight não é mais necessário

A interface do usuário do console de gerenciamento não requer mais o Silverlight. O console de gerenciamento do 5,1 é criado em HTML5 e JavaScript.

### As notificações e mensagens são exibidas individualmente em uma caixa de diálogo

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Novo no App-V 5,1</th>
<th align="left">Antes do App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Indicador de número de mensagens:</strong></p>
<p>Na barra de título do console de gerenciamento do App-V, um número agora é exibido ao lado de um ícone de sinalizador para indicar o número de mensagens que estão aguardando para serem lidas.</p></td>
<td align="left"><p>Você pode ver apenas uma mensagem ou um erro de cada vez, e você não pôde determinar quantas mensagens havia.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Aparência da mensagem:</strong></p>
<ul>
<li><p>As mensagens que exigem entrada do usuário aparecem em uma caixa de diálogo separada que é exibida na parte superior da página atual que você estava exibindo e exigem uma resposta antes de poder descartá-las.</p></li>
<li><p>Mensagens e erros aparecem em uma lista, com um abaixo do outro.</p></li>
</ul></td>
<td align="left"><p>Você pode ver apenas uma mensagem ou um erro de cada vez.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Ignorando mensagens:</strong></p>
<p>Use o <strong> link ignorar tudo </strong> para ignorar todas as mensagens e erros de uma vez ou descartá-los um de cada vez.</p></td>
<td align="left"><p>Você pode ignorar mensagens e erros apenas um de cada vez.</p></td>
</tr>
</tbody>
</table>



### As páginas do console agora são URLs separadas

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Novo no App-V 5,1</th>
<th align="left">Antes do App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cada página no console tem uma URL diferente, que permite marcar páginas específicas para acesso rápido no futuro.</p>
<p>O número que aparece em algumas URLs indica o pacote específico. Esses números são exclusivos.</p></td>
<td align="left"><p>Todas as páginas de console são acessadas por meio da mesma URL.</p></td>
</tr>
</tbody>
</table>



### Nova, página de grupos de conexão separados e opção de menu

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Novo no App-V 5,1</th>
<th align="left">Antes do App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>A página de grupos de conexão agora faz parte do menu principal, no mesmo nível da página de pacotes.</p></td>
<td align="left"><p>Para abrir a página grupos de conexão, navegue pela página pacotes.</p></td>
</tr>
</tbody>
</table>



### As opções de menu para pacotes foram alteradas

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Novo no App-V 5,1</th>
<th align="left">Antes do App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>As opções a seguir são botões agora que aparecem na parte inferior da página pacotes:</p>
<ul>
<li><p>Adicionar ou atualizar</p></li>
<li><p>Publicar</p></li>
<li><p>Cancelar</p></li>
<li><p>Excluir</p></li>
</ul>
<p>As opções a seguir ainda serão exibidas quando você clicar com o botão direito do mouse em um pacote para abrir o menu de contexto suspenso:</p>
<ul>
<li><p>Publicar</p></li>
<li><p>Cancelar</p></li>
<li><p>Editar o acesso ao anúncio</p></li>
<li><p>Editar configuração de implantação</p></li>
<li><p>Transferir configuração de implantação de...</p></li>
<li><p>Transferir acesso e configuração de...</p></li>
<li><p>Excluir</p></li>
</ul>
<p>Quando você clica em <strong> excluir </strong> para remover um pacote, uma caixa de diálogo é aberta e solicita que você confirme que deseja excluir o pacote.</p></td>
<td align="left"><p>A <strong> opção Adicionar ou atualizar </strong> era um botão no canto superior direito da página pacotes.</p>
<p>As <strong> </strong> Opções publicar, <strong> Cancelar publicação </strong> e <strong> excluir </strong> estavam disponíveis somente se você clicar com o botão direito do mouse em um nome de pacote na lista pacotes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>As seguintes operações de pacote agora são botões na página de detalhes do pacote para cada pacote:</p>
<ul>
<li><p>Transferir (menu suspenso com as seguintes opções):</p>
<ul>
<li><p>Transferir configuração de implantação de...</p></li>
<li><p>Transferir acesso e configuração de...</p></li>
</ul></li>
<li><p>Editar (grupos de conexão e acesso ao AD)</p></li>
<li><p>Cancelar</p></li>
<li><p>Excluir</p></li>
<li><p>Editar configuração padrão</p></li>
</ul></td>
<td align="left"><p>Essas opções de pacote estavam disponíveis somente se você clicar com o botão direito do mouse em um nome de pacote na lista pacotes.</p></td>
</tr>
</tbody>
</table>



### Ícones no painel esquerdo têm novas cores e texto

As cores dos ícones no painel esquerdo foram alteradas e o texto é adicionado para tornar os ícones consistentes com outros produtos da Microsoft.

### A página de visão geral foi removida

No painel esquerdo do console de gerenciamento, a opção de menu visão geral e sua página de visão geral associada foram removidas.

### <a href="" id="bkmk-seqimprove"></a>Melhorias do sequenciador

Os seguintes aprimoramentos foram feitos no editor de pacotes no sequenciador do App-V 5,1.

### Importar e exportar o arquivo de manifesto

Você pode importar e exportar o arquivo AppxManifest.xml. Para exportar o arquivo de manifesto, selecione a guia **avançado** e, na caixa arquivo de manifesto, clique em **Exportar..**.. Você pode fazer alterações no arquivo de manifesto, como a remoção de extensões do Shell ou a edição de associações de tipo de arquivo.

Depois de fazer as alterações, clique em **importar...** e selecione o arquivo editado. Depois de importá-lo com êxito novamente, o arquivo de manifesto será atualizado imediatamente dentro do editor do pacote.

**Tenha**  
Quando você importa o arquivo, suas alterações são validadas em relação ao esquema XML. Se o arquivo não for válido, você receberá um erro. Lembre-se de que é possível importar um arquivo validado em relação ao esquema XML, mas que ainda poderá falhar para ser executado por outros motivos.



### Adição da lista de Windows 10 a sistemas operacionais

Na guia implantação, os bits do Windows 10 32-bit e do Windows 10-64 foram adicionados à lista de sistemas operacionais para os quais você pode sequenciar um pacote. Se você selecionar **qualquer sistema operacional**, o Windows 10 será incluído automaticamente entre os sistemas operacionais aos quais o pacote sequenciado dará suporte.

### O caminho atual é exibido na parte inferior do editor do registro virtual

Na guia registro virtual, o caminho agora é exibido na parte inferior do editor do registro virtual, que permite que você determine a chave atualmente selecionada. Antes, era preciso rolar pela árvore do registro para localizar a chave atualmente selecionada.

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a>Caixa de diálogo "localizar e substituir" combinada e teclas de atalho adicionadas no editor do registro virtual

No editor de registro virtual, as teclas de atalho foram adicionadas à opção Localizar (Ctrl + F) e uma caixa de diálogo que combina as tarefas "localizar" e "substituir" foi adicionada para permitir que você localize e substitua valores e dados. Para acessar essa caixa de diálogo combinada, selecione uma chave e siga um destes procedimentos:

-   Pressione **Ctrl + H**

-   Clique com o botão direito do mouse em uma tecla e selecione **substituir**.

-   Selecione **Exibir** &gt; **substituir registro virtual** &gt; **Replace**.

Anteriormente, a caixa de diálogo "substituir" não existe e você precisava fazer alterações manualmente.

### Renomear chaves de registro e arquivos de pacote com êxito

Você pode renomear arquivos e chaves do registro virtual sem ter problemas com o sequenciador. Anteriormente, o sequenciador parou de funcionar se você tentou renomear uma chave.

### Importar e exportar chaves do registro virtual

Você pode importar e exportar chaves do registro virtual. Para importar uma chave, clique com o botão direito do mouse no nó sob o qual deseja importar a chave, navegue até a tecla que você deseja importar e clique em **importar**. Para exportar uma chave, clique com o botão direito do mouse na chave e selecione **Exportar**.

### Importar um diretório para o sistema de arquivos virtual

Você pode importar um diretório para o VFS. Para importar um diretório, clique na guia **arquivos de pacote** e, em seguida, clique em **Exibir** &gt; diretório de importação do sistema de **arquivos virtual** &gt; **Import Directory**. Se você tentar importar um diretório que contém arquivos que já estão no VFS, a importação falhará e uma mensagem explicativa será exibida. Antes do App-V 5,1, não foi possível importar diretórios.

### Importar ou exportar um arquivo VFS sem precisar excluí-lo e adicioná-lo novamente ao pacote

Você pode importar arquivos ou exportar arquivos do VFS sem precisar excluir o arquivo e adicioná-lo novamente ao pacote. Por exemplo, você pode usar esse recurso para exportar um log de alterações para uma unidade local, editar o arquivo usando um editor externo e, em seguida, importar novamente o arquivo para o VFS.

Para exportar um arquivo, selecione a guia **arquivos de pacote** , clique com o botão direito do mouse no arquivo no VFS, clique em **Exportar**e escolha um local de exportação do qual você pode fazer as edições.

Para importar um arquivo, selecione a guia **arquivos de pacote** e clique com o botão direito do mouse no arquivo que você exportou. Navegue até o arquivo editado e clique em **importar**. O arquivo importado substituirá o arquivo existente.

Depois de importar um arquivo, você deve salvar o pacote clicando em **File** &gt; **salvar**arquivo.

### O menu para adicionar um arquivo de pacote foi movido

A opção de menu para adicionar um arquivo de pacote foi movida. Para localizar a opção Adicionar, selecione a guia **arquivos de pacote** e, em seguida, clique em **Exibir** &gt; **sistema de arquivos virtual** &gt; **Adicionar arquivo**. Anteriormente, você clicou com o botão direito do mouse em uma pasta no nó VFS e escolhe **Adicionar arquivo**.

### Nó do registro virtual expande hives do computador e do usuário por padrão

Quando você abre o registro virtual, as hives do computador e do usuário são mostradas abaixo do nó do registro de nível superior. Antes, era preciso expandir o nó do registro para mostrar as Hives abaixo.

### Habilitar ou desabilitar objetos auxiliares do navegador

Você pode habilitar ou desabilitar objetos auxiliares do navegador selecionando uma nova caixa de seleção, habilitar objetos auxiliares do navegador, na guia Avançado da interface de usuário do sequenciador. Se objetos auxiliares do navegador:

-   Existir no pacote e estiver habilitada, a caixa de seleção estará marcada por padrão.

-   Existir no pacote e estiverem desativados, a caixa de seleção estará desmarcada por padrão.

-   Existe no pacote, com um ou mais habilitado e um ou mais desabilitado, a caixa de seleção é definida como indeterminada por padrão.

-   Não existir no pacote, a caixa de seleção estará desabilitada.

### <a href="" id="bkmk-pkgconvimprove"></a>Melhorias no conversor de pacote

Agora você pode usar o conversor de pacote para converter pacotes do App-V 4,6 que contêm scripts e informações do registro e scripts dos arquivos Source. OSD agora estão incluídos na saída do conversor de pacote.

Para obter mais informações, incluindo exemplos, confira [migrar para o App-V 5,1 de uma versão anterior](migrating-to-app-v-51-from-a-previous-version.md).

### <a href="" id="bkmk-supmultscripts"></a>Suporte para vários scripts em um único gatilho de evento

O App-V 5,1 oferece suporte ao uso de vários scripts em um único gatilho de evento para pacotes do App-V, incluindo pacotes que você está convertendo do App-V 4,6 para o App-V 5,0 ou posterior. Para habilitar o uso de vários scripts, o App-V 5,1 usa um aplicativo inicializador de scripts, chamado ScriptRunner.exe, que é instalado como parte da instalação do App-V Client.

Para obter mais informações, incluindo uma lista de gatilhos de eventos e o contexto em que scripts podem ser executados, consulte a seção scripts em [sobre a configuração dinâmica do App-V 5,1](about-app-v-51-dynamic-configuration.md).

### <a href="" id="bkmk-hardcodepath"></a>Caminho codificado para a pasta de instalação é redirecionado para a raiz do sistema de arquivos virtual

Quando você converte pacotes do App-V 4,6 para o 5,1, o pacote App-V 5,1 pode acessar a unidade codificada que você era obrigado a usar quando criou pacotes do 4,6. A letra da unidade será a unidade que você selecionou como a unidade de instalação na máquina de sequenciamento de 4,6. (A letra da unidade padrão é Q:\\.)

Anteriormente, a pasta raiz do 4,6 não foi reconhecida e não pôde ser acessada pelos pacotes do App-V 5,0. Os pacotes do App-V 5,1 podem acessar arquivos codificados por seu caminho completo ou podem enumerar programaticamente arquivos na raiz de instalação do App-V 4,6.

**Detalhes técnicos:** O conversor de pacotes do App-V 5,1 salvará a pasta raiz de instalação do App-V 4,6 e nomes de pastas curtas no arquivo FilesystemMetadata.xml do elemento FileSystem. Quando o cliente App-V 5,1 cria o processo virtual, ele mapeará solicitações da raiz de instalação do App-V 4,6 para a raiz do sistema de arquivos virtual.

## Como obter tecnologias do MDOP


O App-V faz parte do Microsoft Desktop Optimization Pack (MDOP). O MDOP faz parte do Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte [como faço para obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Tópicos relacionados


[Notas de versão do App-V 5.1](release-notes-for-app-v-51.md)









