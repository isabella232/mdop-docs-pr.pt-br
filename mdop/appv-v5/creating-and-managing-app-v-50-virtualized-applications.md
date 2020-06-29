---
title: Criação e gerenciamento de aplicativos virtualizados App-V 5.0
description: Criação e gerenciamento de aplicativos virtualizados App-V 5.0
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796565"
---
# Criação e gerenciamento de aplicativos virtualizados App-V 5.0


Depois de implantar corretamente o sequenciador do Microsoft Application Virtualization (App-V) 5,0, você pode usá-lo para monitorar e gravar o processo de instalação e configuração para que um aplicativo seja executado como um aplicativo virtualizado.

**Observação**  Para obter mais informações sobre como configurar o sequenciador do Microsoft Application Virtualization (App-V) 5,0, as práticas recomendadas de sequenciamento e um exemplo de como criar e atualizar um aplicativo virtual, consulte o [Guia de sequenciamento do Microsoft Application Virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0 sequenciating Guide.docx).

 

## Sequenciando um aplicativo


Você pode usar o sequenciador do App-V 5,0 para executar as seguintes tarefas:

-   Crie pacotes virtuais que podem ser implantados em computadores que executam o cliente App-V 5,0.

-   Atualize os pacotes existentes. Você pode expandir um pacote existente no computador executando o sequenciador e, em seguida, atualizar o aplicativo para criar uma versão mais recente.

-   Edite informações de configuração associadas a um pacote existente. Por exemplo, você pode adicionar um atalho ou modificar uma associação de tipo de arquivo.

    **Observação**  Você deve criar atalhos e salvá-los em um local de rede disponível para permitir o roaming. Se um atalho é criado e salvo em um local privado, o pacote deve ser publicado localmente no computador executando o cliente App-V 5,0.

     

-   Converter pacotes virtuais existentes.

O sequenciador usa o diretório **% tmp% \ \ Scratch** ou **% Temp% \ \ Scratch** e o diretório **Temp** para armazenar arquivos temporários durante o sequenciamento. No computador que executa o sequenciador, você deve configurar esses diretórios com espaço livre em disco equivalente aos requisitos de instalação de aplicativo estimados. Configurar os diretórios temporários e o diretório Temp em partições de disco rígido diferentes podem ajudar a melhorar o desempenho durante o sequenciamento.

Quando você usa o sequenciador para criar um novo aplicativo virtual, os seguintes arquivos listados são criados. Esses arquivos compreendem o pacote App-V 5,0.

-   arquivo. msi. Este arquivo do Windows Installer (. msi) é criado pelo sequenciador e é usado para instalar o pacote virtual em computadores de destino.

-   Arquivo Report.xml. Nesse arquivo, o sequenciador salva todos os problemas, avisos e erros que foram descobertos durante o sequenciamento. Ele exibe as informações após a criação do pacote. Você pode nos reenviar para o diagnóstico e a solução de problemas.

-   arquivo. AppV. Este é o arquivo de aplicativo virtual.

-   Arquivo de configuração de implantação. O arquivo de configuração de implantação determina como o aplicativo virtual será implantado nos computadores de destino.

-   Arquivo de configuração do usuário. O arquivo de configuração do usuário determina como o aplicativo virtual será executado em computadores de destino.

**Importante**  Você deve configurar as pastas% TMP% e% TEMP% que o conversor de pacote usa para ser um local seguro e um diretório. Um local seguro está acessível somente por um administrador. Além disso, quando você sequenciar o pacote, salve o pacote em um local seguro ou certifique-se de que nenhum outro usuário tenha permissão para estar conectado durante o processo de conversão e monitoramento.

 

A caixa de diálogo **Opções** no console do sequenciador contém as seguintes guias:

-   **Geral**. Use esta guia para habilitar as atualizações da Microsoft para serem executadas durante o sequenciamento. Selecione **acrescentar versão do pacote ao nome do arquivo** para configurar a sequência para adicionar um número de versão ao pacote virtualizado que está sendo sequenciado. Selecione **sempre confiar na fonte dos aceleradores de pacote** para criar pacotes virtualizados usando um acelerador de pacote sem precisar de autorização.

    **Importante**  Aceleradores de pacote criados usando o App-V 4.6 não são compatíveis com o App-V 5,0.

     

-   **Analisar itens**. Esta guia exibe os locais de caminho de arquivo associados que serão analisados ou emsinaláveis no ambiente virtual. Os tokens são úteis para adicionar arquivos usando a guia **arquivos de pacote** em **edição avançada**.

-   **Itens de exclusão**. Use esta guia para especificar quais pastas e diretórios não devem ser monitorados durante a sequenciagem. Para adicionar dados de aplicativo locais salvos na pasta dados do aplicativo local no pacote, clique em **novo** e especifique o local e o tipo de **mapeamento**associado. Essa opção é necessária para alguns pacotes.

O App-V 5,0 dá suporte a aplicativos que incluem serviços do Microsoft Windows. Se um aplicativo incluir um serviço do Windows, o serviço será incluído no pacote virtual sequenciado desde que seja instalado enquanto estiver sendo monitorado pelo sequenciador. Se um aplicativo virtual criar um serviço do Windows quando ele for executado inicialmente, depois, posteriormente, após a instalação, o aplicativo deverá ser executado enquanto o sequenciador estiver sendo monitorado para que o serviço do Windows seja adicionado ao pacote. Só há suporte para serviços que são executados na conta do sistema local. Os serviços que são configurados para o AutoStart ou o AutoStart atrasar são iniciados antes do primeiro aplicativo virtual em um pacote ser executado dentro do ambiente virtual do pacote. Os serviços do Windows que estão configurados para serem iniciados sob demanda por um aplicativo são iniciados quando o aplicativo virtual dentro do pacote inicia o serviço por meio da chamada de API.

[Como sequenciar um novo aplicativo com o App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> Suporte à extensão do shell do App-V 5.0 SP2


O App-V 5.0 SP2 oferece suporte a extensões do Shell. As extensões do Shell serão detectadas e inseridas no pacote durante o sequenciamento.

Extensões do shell são incorporadas ao pacote automaticamente durante o processo de sequenciamento. Quando o pacote for publicado, a extensão do Shell fornecerá aos usuários a mesma funcionalidade do que se o aplicativo fosse instalado localmente.

**Requisitos para usar extensões do Shell:**

-   Os pacotes que contêm extensões de shell inseridas devem ser publicados globalmente. O aplicativo não requer configuração adicional ou configuração no cliente para habilitar a funcionalidade de extensão do Shell.

-   O "" bits "do aplicativo, o Sequencer e o cliente App-V devem corresponder ou as extensões do shell não funcionarão. Por exemplo:

    -   A versão do aplicativo é de 64 bits.

    -   O sequenciador está em execução em um computador de 64 bits.

    -   O pacote está sendo entregue a um computador cliente do App-V do 64-bit.

A tabela a seguir lista as extensões do shell com suporte:

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
<td align="left"><p>Controla a ação na qual clique com o botão direito do mouse, arraste e solte e modifique o menu de contexto exibido.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de destino soltar</p></td>
<td align="left"><p>Controla a ação após a arrastar e soltar um objeto de dados em um destino de soltura, como um arquivo.</p></td>
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
<td align="left"><p>Permite a recuperação de sinalizadores e informações de infotip de um item e a exibição dentro de uma dica de ferramenta pop-up durante o foco do mouse.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manipulador de colunas</p></td>
<td align="left"><p>Permite criar e exibir colunas personalizadas no <strong> modo de exibição de detalhes do Windows Explorer </strong> . Ele pode ser usado para estender a classificação e o agrupamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gerenciador de visualização</p></td>
<td align="left"><p>Permite que uma visualização de um arquivo seja exibida no painel de visualização do Windows Explorer.</p></td>
</tr>
</tbody>
</table>

 

## Suporte à extensão de arquivo Copy on Write (vaca)


As extensões de arquivo Copy on Write (vaca) permitem que o App-V 5,0 grave dinamicamente em locais específicos contidos no pacote virtual enquanto ele está sendo usado.

A tabela a seguir exibe os tipos de arquivo que podem existir em um pacote virtual no diretório VFS, mas não pode ser atualizado no computador que executa o cliente App-V 5,0. Todos os outros arquivos e diretórios podem ser modificados.

. ACM

. asa

.asp

. aspx

. AX

.bat

.cer

.chm

. CLB

.cmd

.cnt

.cnv

.com

.cpl

.cpx

.crt

.dll

.drv

.exe

.fon

.grp

.hlp

.hta

. IME

.inf

.ins

.isp

. seu

.js

.jse

.lnk

.msc

.msi

.msp

.mst

. mui

. NLS

.ocx

. PAL

.pcd

.pif

.reg

.scf

.scr

. SCT

.shb

.shs

.sys

. tlb

. tsp

.url

.vb

.vbe

.vbs

.vsmacros

.ws

. ESC

.wsf

.wsh

 

## Modificando um pacote de aplicativo virtual existente


Você pode usar o sequenciador para modificar um pacote existente. O computador no qual você faz isso deve corresponder à arquitetura de chip do computador usado para criar o aplicativo. Por exemplo, se você inicialmente sequenciava um pacote usando um computador que executa um sistema operacional de 64 bits, deve modificá-lo usando um computador que esteja executando um sistema operacional de 64 bits.

[Como modificar um pacote de aplicativo virtual existente](how-to-modify-an-existing-virtual-application-package-beta.md)

## Criando um modelo de projeto


Um arquivo. appvt é um modelo de projeto que pode ser usado para salvar configurações personalizadas e comumente aplicadas. Você pode usar mais facilmente essas configurações para sequenciais futuros.

Os modelos de projeto do App-V 5,0 diferem dos aceleradores de aplicativos do App-V 5,0 porque o App-V 5,0 Application Accelerators são específicos do aplicativo e os modelos de projeto do App-V 5,0 podem ser aplicados a vários aplicativos. Além disso, você não pode usar um modelo de projeto quando usa um acelerador de pacote para criar um pacote de aplicativo virtual. As seguintes configurações gerais são salvas com um modelo de projeto App-V 5,0:

Um modelo pode especificar e armazenar várias configurações da seguinte maneira:

-   **Opções avançadas de monitoramento**. Permite que o Microsoft Update seja executado durante o monitoramento. Salva as configurações da opção permitir interação local

-   **Opções gerais**. Habilita o uso do **Windows Installer**, **acrescenta a versão do pacote ao nome do arquivo**.

-   **Itens de exclusão.** Contém a lista de padrões de exclusão.

[Como criar e usar um modelo de projeto](how-to-create-and-use-a-project-template.md)

## Criando um acelerador de pacote


**Observação**  Os aceleradores de pacote criados usando uma versão anterior do App-V devem ser recriados usando o App-V 5,0.

 

Você pode usar aceleradores de pacotes do App-V 5,0 para gerar automaticamente novos pacotes de aplicativos virtuais. Depois de criar um acelerador de pacote com êxito, você poderá reutilizar e compartilhar o acelerador de pacote.

Em algumas situações, para criar o acelerador de pacote, talvez seja necessário instalar o aplicativo localmente no computador que executa o sequenciador. Nesses casos, você deve primeiro tentar criar o acelerador de pacote com a mídia de instalação. Se vários arquivos ausentes forem necessários, instale o aplicativo localmente no computador que executa o sequenciador e, em seguida, crie o acelerador de pacote.

Depois de criar um acelerador de pacote com êxito, você poderá reutilizar e compartilhar o acelerador de pacote. A criação de aceleradores de pacotes do App-V 5,0 é uma tarefa avançada. Os aceleradores de pacote podem conter informações específicas de senha e usuário. Portanto, você deve salvar aceleradores de pacote e a mídia de instalação associada em um local seguro, e deve assinar digitalmente o acelerador de pacote depois de criá-lo para que o fornecedor possa ser verificado quando o acelerador de pacotes do App-V 5,0 for aplicado.

[Como criar um acelerador de pacote](how-to-create-a-package-accelerator.md)

[Como criar um pacote de aplicativo virtual usando um acelerador de pacote do App-V](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## Relatório de erros do sequenciador


O sequenciador do App-V 5,0 pode detectar problemas de sequenciamento comuns durante o sequenciamento. A página **relatório de instalação** no final do assistente de sequenciamento exibe as mensagens de diagnóstico categorizadas em **erros**, **avisos**e **informações** dependendo da gravidade do problema.

Você também pode encontrar informações adicionais sobre o sequenciamento de erros usando o Visualizador de eventos do Windows.






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a>Outros recursos para o sequenciador do App-V 5,0


-   [Operações para o App-V 5.0](operations-for-app-v-50.md)

 

 





