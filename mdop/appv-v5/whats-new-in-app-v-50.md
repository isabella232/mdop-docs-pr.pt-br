---
title: Quais são as novidades no App-V 5.0
description: Quais são as novidades no App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796195"
---
# Quais são as novidades no App-V 5.0


Esta seção é para os usuários que já estão familiarizados com o App-V e querem saber o que mudou no App-V 5,0 se você ainda não estiver familiarizado com o App-V, deve começar por meio [de leitura de planejamento para o app-v 5,0](planning-for-app-v-50-rc.md).

## Alterações na funcionalidade padrão


As seções a seguir contêm informações sobre as alterações na funcionalidade padrão do App-V 5,0.

### Alterações em sistemas operacionais com suporte

Para obter mais informações, consulte [configurações compatíveis do App-V 5,0](app-v-50-supported-configurations.md).

## Alterações no sequenciador


As seções a seguir contêm informações sobre as alterações no sequenciador do App-V 5,0.

### Alteração específica no sequenciador

A tabela a seguir exibe informações sobre o que mudou com o sequenciador do App-V 5,0

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Recurso sequenciador</th>
<th align="left">Funcionalidade do sequenciador do App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processamento de reinicialização</p></td>
<td align="left"><p>Quando um aplicativo solicita uma reinicialização, você deve permitir que o aplicativo reinicie o computador que executa o sequenciador. O computador executando o sequenciador será reiniciado e o sequenciador será retomado no modo de monitoramento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Especificando o diretório de aplicativos virtual</p></td>
<td align="left"><p>Diretório de aplicativos virtual é um parâmetro obrigatório. Para obter os melhores resultados, ele deve corresponder ao diretório de instalação do instalador do aplicativo. Isso resulta em desempenho e compatibilidade de aplicativos mais ótimos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Editando atalhos/FTAs</p></td>
<td align="left"><p>A página atalhos/FTA está na <strong> </strong> página edição avançada após a conclusão do assistente de sequenciamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Guia Histórico de Alterações</p></td>
<td align="left"><p>A guia alterar histórico foi removida para o App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Guia OSD</p></td>
<td align="left"><p>A guia OSD foi removida para o App-V 5,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Guia Serviços virtuais</p></td>
<td align="left"><p>A guia de serviços virtuais foi removida para o App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Guia arquivos/sistema de arquivos virtual</p></td>
<td align="left"><p>Essas guias são combinadas e permitem que você modifique arquivos de pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Guia Implantação</p></td>
<td align="left"><p>Não há mais opções para configurar a URL do servidor nos pacotes. Você deve configurá-lo agora usando a configuração de implantação ou o servidor de gerenciamento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ferramenta conversor de pacote</p></td>
<td align="left"><p>Agora você pode usar o PowerShell para converter os pacotes criados em versões anteriores.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Complemento/middleware</p></td>
<td align="left"><p>Você pode expandir pacotes pai ao sequenciar um aplicativo complementar ou middleware. Complementos e pacotes middleware devem ser conectados usando grupos de conexão no App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Saída de arquivos</p></td>
<td align="left"><p>Os arquivos a seguir são criados com o App-V 5,0, o Windows Installer (. msi),. AppV, a configuração de implantação, a configuração do usuário e o Report.XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pacotes de compactação/descritores de segurança/MSI</p></td>
<td align="left"><p>A compactação e a criação de um arquivo do Windows Installer (. msi) são automáticas para todos os pacotes, e você não pode mais substituir descritores de segurança.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ferramentas/opções</p></td>
<td align="left"><p>A janela diagnóstico foi removida e várias outras configurações.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unidade de instalação</p></td>
<td align="left"><p>Uma unidade de instalação não é mais necessária quando você instala um aplicativo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Transmissão de OOS</p></td>
<td align="left"><p>Se nenhuma otimização de fluxo for executada, os pacotes serão transportados com falha quando forem solicitados por computadores que executam o cliente App-V 5,0 até que possam ser iniciados.</p></td>
</tr>
<tr class="even">
<td align="left"><p>P: &lt; /p&gt;</td>
<td align="left"><p>O App-V 5,0 usa o sistema de arquivos nativo e não requer mais um Q:.</p></td>
</tr>
</tbody>
</table>

 

## Detecção de erros de sequenciamento


O sequenciador do App-V 5,0 pode detectar problemas de sequenciamento comuns durante o sequenciamento. A página **relatório de instalação** no final do assistente de sequenciamento exibe as mensagens de diagnóstico categorizadas em **erros**, **avisos**e **informações** dependendo da gravidade do problema.

Para exibir informações mais detalhadas sobre um evento, clique duas vezes no item que você deseja revisar no relatório. Os problemas de sequenciamento, bem como sugestões sobre como resolver os problemas são exibidos. As informações do relatório de preparação do sistema e do relatório de instalação serão resumidas quando você terminar de criar um pacote. A lista a seguir mostra os tipos de problemas disponíveis no relatório:

-   Arquivos excluídos.

-   Informações do driver.

-   Diferenças do sistema COM+.

-   Conflitos lado a lado (SxS).

-   Extensões do Shell.

-   Informações sobre serviços sem suporte.

-   Protocolo.

## Grupos de conexão


O recurso App-V anteriormente conhecido como **composição do pacote dinâmico** agora é conhecido como **grupos de conexão** no App-V 5,0. Para obter mais informações sobre como usar grupos de conexão, consulte [Gerenciando grupos de conexão](managing-connection-groups.md).

## Funcionalidade de licenciamento e medição


A funcionalidade de aplicativo e licenciamento foi removida no App-V 5,0. As posições de licença reais em seu ambiente dependem da licença de título de software específica e dos direitos de uso concedidos pelos termos de licença associados.

## Cache de arquivos e aplicativos


Não há arquivo ou cache de aplicativos disponível com o App-V 5,0.






## Tópicos relacionados


[Sobre o App-V 5.0](about-app-v-50.md)

 

 





