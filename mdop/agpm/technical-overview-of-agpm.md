---
title: Visão geral técnica do AGPM
description: Visão geral técnica do AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797297"
---
# Visão geral técnica do AGPM


O gerenciamento avançado de política de grupo (AGPM) da Microsoft é um aplicativo cliente/servidor. O servidor do AGPM armazena objetos de política de grupo (GPOs) offline no arquivo morto que o AGPM cria no sistema de arquivos do servidor. Os administradores de política de grupo usam o snap-in do AGPM para o console de gerenciamento de política de grupo (GPMC) para trabalhar com GPOs no servidor que hospeda o arquivo morto. Compreender as partes do AGPM e dos itens relacionados, como eles armazenam os GPOs no sistema de arquivos e como as permissões controlam as ações disponíveis para cada função de usuário podem melhorar a eficácia dos administradores de política de grupo com o AGPM.

## Terminologia


A seguir está a explicação dos termos básicos do AGPM.

-   **Cliente do AGPM:** Um computador que executa o snap-in do AGPM para o console de gerenciamento de política de grupo (GPMC) e de quais administradores de política de grupo gerenciam GPOs.

-   **Snap-in do AGPM:** O componente de software do AGPM instalado em clientes do AGPM para que eles possam gerenciar GPOs.

-   **Servidor do AGPM:** Um servidor que executa o serviço do AGPM e gerencia um arquivo morto. Cada servidor do AGPM pode gerenciar apenas um arquivo, mas um servidor do AGPM pode gerenciar dados de arquivo para vários domínios em um arquivo. Um arquivo pode ser hospedado em um computador que não seja um servidor do AGPM.

-   **Serviço do AGPM:** O componente de software do AGPM que é executado em um servidor do AGPM como um serviço. O serviço gerencia GPOs no arquivo morto e no ambiente de produção dessa floresta.

-   **Arquivo morto:** No AGPM, um repositório central que contém os GPOs controlados que o servidor do AGPM associado gerencia, além do histórico de cada um desses GPOs. Isso inclui todas as versões controladas anteriores de cada GPO. Um arquivo consiste em um arquivo de índice de arquivo morto e dados de arquivo morto associados que podem incluir dados para GPOs em vários domínios. Um arquivo pode ser hospedado em um computador que não seja um servidor do AGPM.

-   **GPO controlado:** Um GPO que está sendo gerenciado pelo AGPM. O AGPM gerencia o histórico e as permissões dos GPOs controlados, que são armazenados no arquivo morto.

-   **GPO não controlado:** Um GPO no ambiente de produção para um domínio e não é gerenciado pelo AGPM.

## O que o AGPM instala, cria e afeta


Em um servidor do AGPM, o programa de instalação do AGPM instala o serviço do AGPM. O AGPM não altera o serviço de diretório® do Active Directory ou o esquema. Por padrão, os arquivos de programa do servidor do AGPM são instalados no%ProgramFiles%\\Microsoft\\AGPM\\Server. Você pode instalar o serviço do AGPM em um controlador de domínio se precisar; no entanto, recomendamos que você instale o serviço do AGPM em um servidor membro.

Em um cliente do AGPM, o programa de instalação do AGPM instala o snap-in do AGPM, adicionando uma pasta de **controle de alterações** a cada domínio exibido no GPMC. Por padrão, os arquivos do programa cliente do AGPM são instalados no%ProgramFiles%\\Microsoft\\AGPM\\Client.

A tabela 1 descreve os itens que o AGPM instala ou cria e as partes do sistema operacional que afetam a operação do AGPM.

**Tabela 1: itens instalados, criados ou afetados pelo AGPM**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Item</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serviço do AGPM</p></td>
<td align="left"><p>O serviço do AGPM é executado no servidor do AGPM. O serviço gerencia o arquivo morto, que contém GPOs offline e GPOs controlados no ambiente de produção. A configuração padrão do serviço do AGPM é a seguinte:</p>
<ul>
<li><p><strong>Nome do serviço: </strong> serviço do AGPM</p></li>
<li><p><strong>Nome para exibição: </strong> serviço do AGPM</p></li>
<li><p><strong>Caminho para executável: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</p></li>
<li><p><strong>Inicialização: </strong> automática</p></li>
<li><p><strong>Faça logon como: </strong> conta de serviço do AGPM especificada durante a instalação do servidor do AGPM, que pode ser alterada usando <strong> programas e recursos </strong> no <strong> painel de controle </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Arquivo do AGPM</p></td>
<td align="left"><p>Por padrão, o AGPM cria o arquivo morto no%ProgramData%\Microsoft\AGPM no servidor do AGPM. O arquivo fornece armazenamento para GPOs offline e pode armazenar várias versões de cada GPO. As alterações que o AGPM faz nos GPOs no arquivo não afetam o ambiente de produção até que um administrador do AGPM ou o aprovador implante o GPO no ambiente de produção e vincule o GPO a uma unidade organizacional (OU).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Firewall do Windows</p></td>
<td align="left"><p>Durante a instalação, o AGPM permite uma regra de firewall de entrada do Windows que permite que o cliente do AGPM se comunique com o servidor do AGPM. A regra padrão do firewall do Windows é a seguinte:</p>
<ul>
<li><p><strong>Nome: </strong> serviço do AGPM</p></li>
<li><p><strong>Ação: </strong> permitir a conexão</p></li>
<li><p><strong>Programas: </strong> todos os programas que atendem às condições especificadas</p></li>
<li><p><strong>Tipo de protocolo: </strong> TCP</p></li>
<li><p><strong>Porta local: </strong> 4600</p></li>
<li><p><strong>Porta remota: </strong> todas as portas</p></li>
<li><p><strong>Endereço IP local: </strong> qualquer</p></li>
<li><p><strong>Endereço IP remoto: </strong> qualquer</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de email</p></td>
<td align="left"><p>O AGPM usa SMTP (Simple Mail Transfer Protocol) para enviar solicitações de email para os endereços configurados na <strong> Guia de delegação de domínio </strong> . Por exemplo, quando um editor solicita que um novo GPO seja criado, o AGPM notifica cada endereço de email especificado na <strong> Guia de delegação de domínio </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Snap-in do AGPM</p></td>
<td align="left"><p>O snap-in do AGPM para o GPMC é executado em clientes do AGPM e é usado por administradores de política de grupo para gerenciar GPOs. O snap-in é exibido no GPMC como uma <strong> pasta controle de alterações </strong> em cada domínio.</p></td>
</tr>
</tbody>
</table>

 

### Referências adicionais

Para obter mais informações sobre os arquivos instalados pelo AGPM, consulte o [Guia de planejamento para o AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).

## Archive


Por padrão, o processo de instalação do servidor do AGPM cria o arquivo no disco rígido local do servidor do AGPM em%ProgramData%\\Microsoft\\AGPM. No entanto, você pode alterar o caminho durante a instalação e até mesmo criar o arquivo morto em um servidor que não seja o servidor do AGPM.

O arquivo contém uma subpasta para cada versão de cada GPO que o arquivo contém. O nome de cada subpasta é um GUID que identifica uma versão do GPO.

O arquivo gpostate.xml registra o estado de cada GPO no arquivo morto. O arquivo é um manifesto que descreve o conteúdo do arquivo morto. Por exemplo, um GPO pode ter várias versões, e cada versão está em sua própria subpasta no arquivo. O arquivo gpostate.xml indica quais subpastas contêm versões diferentes de um único GPO. Além disso, os modelos de GPO têm subpastas no arquivo, mas gpostate.xml indicam que esses são modelos e não GPOs controlados. Da mesma forma, quando os administradores de política de Grupo excluem GPOs, o AGPM altera seus Estados em gpostate.xml para indicar que eles estão na **Lixeira** , mas não remove as subpastas dos GPOs do arquivo morto.

**Cuidado**  Não edite gpostate.xml manualmente ou os GPOs que o arquivo contém. Essas informações são fornecidas apenas para melhorar a compreensão do arquivamento do AGPM. Em vez disso, use o snap-in do AGPM para alterar os GPOs.

 

Quando o AGPM cria o arquivo morto, ele dá controle total a sistema, administradores e conta de serviço do AGPM (especificado na configuração do servidor do AGPM). Alterar permissões usando a interface do usuário do AGPM no snap-in do AGPM não altera permissões no arquivo morto, porque a conta do serviço do AGPM executa todas as operações em nome do usuário conectado.

### Referências adicionais

Para obter informações sobre como fazer backup do arquivo morto, restaurar o arquivo de um backup ou mover o servidor do AGPM e o arquivo morto, consulte a seção "realizando tarefas do administrador do AGPM" no [Guia de operações do AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).

## Funções e permissões


As funções simplificam a delegação. Em vez de atribuir permissões detalhadas a administradores de política de grupo, os administradores do AGPM podem atribuir uma das quatro funções aos administradores de política de grupo para que elas realizem o trabalho relacionado a essa função:

-   **Administrador do AGPM:** Administradores de política de grupo com a função de administrador do AGPM (controle total) atribuídas podem executar qualquer tarefa no AGPM. Os administradores do AGPM podem configurar opções em todo o domínio e delegar permissões para outros administradores de política de grupo.

-   **Aprovador:** Os administradores de política de grupo atribuíram a função de aprovador podem implantar GPOs no ambiente de produção para um domínio. Os aprovadores também podem criar e excluir GPOs e aprovar ou rejeitar solicitações dos editores. Os aprovadores podem exibir a lista de GPOs em um domínio, Visualizar as configurações de política em GPOs e criar e exibir relatórios das configurações de política em um GPO. Não é possível editar as configurações de política nos GPOs, a menos que elas também sejam atribuídas à função de editor.

-   **Editor:** Administradores de política de grupo atribuídos a função de editor podem exibir a lista de GPOs em um domínio, Visualizar as configurações de política em GPOs, editar as configurações de política em GPOs e criar e exibir relatórios das configurações de política em um GPO. A menos que também sejam atribuídas a função de aprovador, os editores não poderão criar, implantar ou excluir GPOs. No entanto, eles podem solicitar que os GPOs sejam criados, implantados ou excluídos.

-   **Revisor:** Administradores de política de grupo atribuídos a função de revisor podem exibir a lista de GPOs em um domínio e criar e exibir relatórios das configurações de política em um GPO. A menos que também sejam atribuídas a função de editor, eles não podem editar as configurações de política em um GPO.

O AGPM proporciona aos administradores do AGPM a flexibilidade de configurar permissões em um nível mais detalhado do que as funções usando o snap-in do AGPM. A tabela 2 descreve essas permissões e indica as permissões concedidas a cada função por padrão.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permissão</th>
<th align="left">Descrição</th>
<th align="left">Administrador do AGPM</th>
<th align="left">Aprovador</th>
<th align="left">Editor</th>
<th align="left">Revisor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Controle total</strong></p></td>
<td align="left"><p>Ter todas as permissões.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Criar GPO</strong></p></td>
<td align="left"><p>Criar GPOs em um domínio.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Conteúdo da lista</strong></p></td>
<td align="left"><p>Listar os GPOs em um domínio.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ler configurações</strong></p></td>
<td align="left"><p>Leia as configurações de política em um GPO.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Editar configurações</strong></p></td>
<td align="left"><p>Altere as configurações de política em um GPO.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Excluir GPO</strong></p></td>
<td align="left"><p>Excluir um GPO.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modificar a segurança</strong></p></td>
<td align="left"><p>Delegar o acesso ao nível do domínio, acessar o acesso a um único GPO e delegar o acesso ao ambiente de produção.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Implantar GPO</strong></p></td>
<td align="left"><p>Implante um GPO do arquivo morto para o ambiente de produção.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Criar modelo</strong></p></td>
<td align="left"><p>Crie um modelo de GPO no AGPM.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Opções de modificação</strong></p></td>
<td align="left"><p>Configurar a notificação de email do AGPM e limitar as versões do GPO armazenadas no arquivo morto.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>GPO de exportação</strong></p></td>
<td align="left"><p>Exportar um GPO para um arquivo.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Importar GPO</strong></p></td>
<td align="left"><p>Importar um GPO de um arquivo.</p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sim</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Observação** 
 As permissões **Exportar GPO** e **importar GPO** não estão disponíveis no AGPM 3,0 ou 2,5.

A capacidade de delegar o acesso a GPOs no ambiente de produção para um domínio e a capacidade de limitar o número de versões de GPO armazenadas não está disponível no AGPM 2,5.

 

### Referências adicionais

Para saber mais sobre quais tarefas podem ser executadas por administradores de política de grupo com uma função específica atribuídas ou sobre quais permissões são necessárias para executar uma tarefa específica, consulte o [Guia de operações para o AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).

 

 





