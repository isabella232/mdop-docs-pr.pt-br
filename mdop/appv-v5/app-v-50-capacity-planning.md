---
title: Planejamento de capacidade do App-V 5.0
description: Planejamento de capacidade do App-V 5.0
author: dansimp
ms.assetid: 56f48b00-cd91-4280-9481-5372a0e2e792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e828457a286f6f686c227a935828679514d87ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796603"
---
# Planejamento de capacidade do App-V 5.0


As seguintes recomendações podem ser usadas como uma linha de base para ajudar a determinar as informações de planejamento de capacidade apropriadas à infraestrutura do App-V do App-5,0 V da sua organização.

**Importante**  Use as informações nesta seção apenas como um guia geral para planejar a implantação do App-V 5,0. Os requisitos de capacidade do sistema dependerão dos detalhes específicos do seu ambiente de hardware e de aplicativos. Além disso, os números de desempenho exibidos neste documento são exemplos e os resultados podem variar.

 

## Determinar o escopo do projeto


Antes de criar a infraestrutura do App-V 5,0, você deve determinar o escopo do projeto. O escopo consiste em determinar quais aplicativos estarão disponíveis virtualmente e também para identificar os usuários de destino e seus locais. Essas informações ajudarão a determinar qual tipo de infraestrutura do App-V 5,0 deve ser implementado. Decisões sobre o escopo do projeto devem ser baseadas nas necessidades específicas da sua organização.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarefa</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Determinar o escopo do aplicativo</p></td>
<td align="left"><p>Dependendo dos aplicativos a serem virtualizados, a infraestrutura do App-V 5,0 pode ser configurada de maneiras diferentes. A primeira tarefa é definir quais aplicativos você deseja virtualizar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Determinar o escopo do local</p></td>
<td align="left"><p>Escopo de localização refere-se aos locais físicos (por exemplo, em toda a empresa ou em uma localização geográfica específica) em que você planeja executar os aplicativos virtualizados. Ele também pode se referir à população do usuário (por exemplo, um único departamento) que irá executar os aplicativos virtuais. Você deve obter um mapa de rede que inclua os caminhos de conexão, bem como a largura de banda disponível para cada local e o número de usuários que usam aplicativos virtualizados e a velocidade do link de WAN.</p></td>
</tr>
</tbody>
</table>

 

## Determine qual é a necessidade de infraestrutura do App-V 5,0


**Importante**  Os dois modelos a seguir exigem que o cliente do App-V 5,0 seja instalado no computador em que você planeja executar aplicativos virtuais.

Você também pode gerenciar seu ambiente do App-V 5,0 usando uma solução ESD (distribuição de software eletrônico), como o Microsoft Systems Center Configuration Manager. Para obter mais informações, consulte [implantando pacotes do App-V 5,0 usando ESD (Electronic Software Distribution)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).

 

-   **Modelo autônomo** – o modelo autônomo permite que aplicativos virtuais sejam habilitados para Windows Installer para distribuição sem streaming. O App-V 5,0 no modo autônomo consiste do sequenciador e do cliente; nenhum componente adicional é necessário. Os aplicativos são preparados para virtualização usando um processo chamado sequenciamento. Para obter mais informações, consulte [planejando o sequenciador do App-V 5,0 e a implantação do cliente](planning-for-the-app-v-50-sequencer-and-client-deployment.md). O modelo autônomo é recomendado para os seguintes cenários:

    -   Com usuários remotos desconectados que não podem se conectar à infraestrutura do App-V 5,0.

    -   Quando você estiver executando um sistema de gerenciamento de software, como o Configuration Manager 2012.

    -   Quando as limitações de largura de banda da rede inibem a distribuição eletrônica de software

-   **Modelo de infra-estrutura completa** : o modelo de infra-estrutura completo oferece recursos de distribuição, gerenciamento e relatórios de software; Ele também inclui o fluxo de aplicativos na rede. O modelo de infraestrutura completa do App-V 5,0 consiste em um ou mais servidores de gerenciamento do App-V 5,0. O servidor de gerenciamento pode ser usado para publicar aplicativos para todos os clientes. O processo de publicação coloca os ícones do aplicativo virtual e os atalhos no computador de destino. Ele também pode transmitir aplicativos para usuários locais. Para obter mais informações sobre como instalar o servidor de gerenciamento, consulte [planejando a implantação do App-V server 5,0](planning-for-the-app-v-50-server-deployment.md). O modelo de infra-estrutura completo é recomendado para os seguintes cenários:

    **Importante**  O modelo de infraestrutura completa do App-V 5,0 exige que o Microsoft SQL Server armazene dados de configuração. Para obter mais informações, consulte [configurações compatíveis com o App-V 5,0](app-v-50-supported-configurations.md).

     

    -   Quando você quiser usar o servidor de gerenciamento para publicar o aplicativo em computadores de destino.

    -   Para o provisionamento rápido de aplicativos para computadores de destino.

    -   Quando quiser usar os relatórios do App-V 5,0.

## Orientação de dimensionamento de servidor ponta a ponta


A seção a seguir fornece informações sobre o planejamento e o planejamento de um App-V 5,0 de ponta a ponta. Para obter informações mais específicas, consulte as seções subsequentes.

**Observação**  Tempo de resposta de ida e volta no cliente é o tempo levado pelo computador executando o cliente App-V 5,0 para receber uma notificação bem-sucedida do servidor de publicação. O tempo de resposta de ida e volta no servidor de publicação é o tempo usado pelo computador que executa o servidor de publicação para receber uma atualização de metadados de pacote bem-sucedida do servidor de gerenciamento.

 

-   Os clientes do 20.000 podem direcionar um único servidor de publicação para obter as atualizações do pacote em um tempo de ida e volta aceitável. ( &lt; 3 segundos)

-   Um único servidor de gerenciamento pode oferecer suporte a até 50 servidores de publicação para atualizações de metadados de pacote em um tempo de ida e volta aceitável. ( &lt; 5 segundos)

## <a href="" id="---------app-v-5-0-management-server-capacity-planning-recommendations"></a> Recomendações de planejamento de capacidade do servidor de gerenciamento do App-V 5,0


Os servidores de publicação do App-V 5,0 exigem o servidor de gerenciamento para solicitações de atualização de pacote e respostas de atualização do pacote. Em seguida, o servidor de gerenciamento envia as informações para o banco de dados de gerenciamento para recuperar informações. Para obter mais informações sobre as configurações compatíveis do App-V 5,0 Management Server [, consulte Configurações compatíveis do App-v 5,0](app-v-50-supported-configurations.md).

**Observação**  O tempo de atualização padrão no servidor de publicação do App-V 5,0 é de dez minutos.

 

Quando vários servidores de publicação simultaneamente entrarem em contato com um único servidor de gerenciamento para atualizações de metadados do pacote, os três fatores a seguir influenciarão o tempo de resposta de ida e volta no servidor de publicação:

1.  Número de servidores de publicação que fazem solicitações simultâneas.

2.  Número de grupos de conexão configurados no servidor de gerenciamento.

3.  Número de grupos de acesso configurados no servidor de gerenciamento.

A tabela a seguir mostra mais informações sobre cada fator que impactam o tempo de viagem de ida e volta.

**Observação**  Tempo de resposta de ida e volta é o tempo usado pelo computador executando o servidor de publicação do App-V 5,0 para receber uma atualização de metadados de pacote bem-sucedida do servidor de gerenciamento.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fatores que afetam o tempo de resposta de ida e volta</th>
<th align="left">Mais informações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>O número de servidores de publicação solicitando atualizações de metadados do pacote simultaneamente.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Um único servidor de gerenciamento pode responder a até 320 servidores de publicação que solicitam metadados de publicação simultaneamente.</p></li>
<li><p>O tempo de resposta de ida e volta para servidores pub do 320 é de aproximadamente 40 segundos.</p></li>
<li><p>Para &lt; servidores de publicação do 50 que solicitam metadados simultaneamente, o tempo de resposta de ida e volta é de &lt; 5 segundos.</p></li>
<li><p>De 50 a 320 servidores de publicação, o tempo de resposta aumenta linearmente (aproximadamente 2x).</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>O número de grupos de conexão configurados no servidor de gerenciamento.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Para até 100 grupos de conexão, não há alteração significativa no tempo de resposta de ida e volta no servidor de publicação.</p></li>
<li><p>Para os grupos de conexão do 100-400, há um aumento linear secundário no tempo de resposta de ida e volta.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>O número de grupos de acesso configurados no servidor de gerenciamento.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Para até 40 grupos de acesso, há um aumento linear (aproximadamente 3x) no tempo de resposta de ida e volta no servidor de publicação.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

A tabela a seguir exibe exemplos de valores para cada um dos fatores anteriores. Em cada variação, os pacotes do 120 são atualizados a partir do App-V 5.0 Management Server.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenário</th>
<th align="left">Variação</th>
<th align="left">Número de grupos de conexão</th>
<th align="left">Número de grupos de acesso</th>
<th align="left">Número de servidores de publicação</th>
<th align="left">Servidor de publicação do tipo de conexão de rede/servidor de gerenciamento</th>
<th align="left">Tempo de resposta de ida e volta no servidor de publicação (em segundos)</th>
<th align="left">Utilização da CPU no servidor de gerenciamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidores de publicação simultaneamente entrando em contato com o servidor de gerenciamento para publicar metadados.</p></td>
<td align="left"><p>Número de servidores de publicação</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>um</p></li>
<li><p>um</p></li>
<li><p>um</p></li>
<li><p>um</p></li>
<li><p>um</p></li>
<li><p>um</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>300</p></li>
<li><p>315</p></li>
<li><p>320</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>5</p></li>
<li><p>254</p></li>
<li><p>pol</p></li>
<li><p>32</p></li>
<li><p>30</p></li>
<li><p>37</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>16</p></li>
<li><p>16</p></li>
<li><p>16</p></li>
<li><p>15</p></li>
<li><p>16</p></li>
<li><p>15</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Metadados de publicação contêm grupos de conexão</p></td>
<td align="left"><p>Número de grupos de conexão</p></td>
<td align="left"><p></p>
<ul>
<li><p>254</p></li>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>150</p></li>
<li><p>300</p></li>
<li><p>400</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>um</p></li>
<li><p>um</p></li>
<li><p>um</p></li>
<li><p>um</p></li>
<li><p>um</p></li>
<li><p>um</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>254</p></li>
<li><p>11:00</p></li>
<li><p>11:00</p></li>
<li><p>16</p></li>
<li><p>22</p></li>
<li><p>25</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>16</p></li>
<li><p>pol</p></li>
<li><p>22</p></li>
<li><p>pol</p></li>
<li><p>cedido</p></li>
<li><p>cedido</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Metadados de publicação contêm grupos de acesso</p></td>
<td align="left"><p>Número de grupos de acesso</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>um</p></li>
<li><p>254</p></li>
<li><p>cedido</p></li>
<li><p>40</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>254</p></li>
<li><p>43</p></li>
<li><p>153</p></li>
<li><p>535</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>16</p></li>
<li><p>26</p></li>
<li><p>24</p></li>
<li><p>24</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

A utilização de CPU do computador que está executando o servidor de gerenciamento está em cerca de 25%, independentemente do número de servidores de publicação direcionados a ele. As transações de banco de dados do Microsoft SQL Server/s, solicitações em lote/s e conexões de usuários são idênticas independentemente do número de servidores de publicação. Por exemplo: transações/s é ~ 30, solicitações em lote ~ 200 e o usuário se conecta aproximadamente 6.

Usando uma implantação geograficamente distribuída, em que o servidor de gerenciamento & servidores de publicação utilizam uma rede de link lento entre eles, o tempo de resposta de ida e volta nos servidores de publicação está dentro dos limites de tempo aceitáveis ( &lt; 5 segundos), mesmo para solicitações simultâneas de 100 em um único servidor de gerenciamento.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenário</th>
<th align="left">Variação</th>
<th align="left">Número de grupos de conexão</th>
<th align="left">Número de grupos de acesso</th>
<th align="left">Número de servidores de publicação</th>
<th align="left">Servidor de publicação do tipo de conexão de rede/servidor de gerenciamento</th>
<th align="left">Tempo de resposta de ida e volta no servidor de publicação (em segundos)</th>
<th align="left">Utilização da CPU no servidor de gerenciamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Conexão de rede entre o servidor de publicação e o servidor de gerenciamento</p></td>
<td align="left"><p>Rede de link lento de 1,5 Mbps</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>um</p></li>
<li><p>um</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Cabo DSL de 1,5 Mbps</p></li>
<li><p>Cabo DSL de 1,5 Mbps</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>4</p></li>
<li><p>5</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>um</p></li>
<li><p>2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Conexão de rede entre o servidor de publicação e o servidor de gerenciamento</p></td>
<td align="left"><p>Rede LAN/WIFI</p></td>
<td align="left"><p></p>
<ul>
<li><p>0</p></li>
<li><p>0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>um</p></li>
<li><p>um</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Wifi</p></li>
<li><p>Wifi</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>11:00</p></li>
<li><p>cedido</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>15</p></li>
<li><p>16</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Se o servidor de gerenciamento e os servidores de publicação estiverem conectados em uma rede de link lento ou em uma rede de alta velocidade, o servidor de gerenciamento pode manipular aproximadamente 15.000 solicitações de atualização de pacote em 30 minutos.

## <a href="" id="---------app-v-5-0-reporting-server-capacity-planning-recommendations"></a> Recomendações de planejamento de capacidade do aplicativo do App-V 5,0 Reporting Server


Os clientes do App-V 5,0 enviam dados de relatório para o servidor de relatórios. Em seguida, o servidor de relatórios registra as informações no banco de dados do Microsoft SQL Server e retorna uma notificação bem-sucedida de volta para o computador que está executando o cliente App-V 5,0. Para obter mais informações sobre as configurações compatíveis do App-V 5,0 Reporting Server, consulte [configurações compatíveis do App-v 5,0](app-v-50-supported-configurations.md).

**Observação**  Tempo de resposta de ida e volta é o tempo usado pelo computador executando o cliente App-V 5,0 para enviar as informações de relatório para o servidor de relatórios e receber uma notificação bem-sucedida do servidor de relatórios.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenário</th>
<th align="left">Resumo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Os clientes do 5,0 do App-V enviam informações de relatório para o servidor de relatórios simultaneamente.</p></td>
<td align="left"><p></p>
<ul>
<li><p>O tempo de resposta de ida e volta do servidor de relatório é de 2,6 segundos para os clientes do 500.</p></li>
<li><p>O tempo de resposta de ida e volta do servidor de relatório é de 5,65 segundos para os clientes do 1000.</p></li>
<li><p>O tempo de resposta de ida e volta aumenta linearmente dependendo do número de clientes.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Solicitações por segundo processadas pelo servidor de relatórios.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Um único servidor de relatórios e um único banco de dados, podem processar um máximo de solicitações 139 por segundo. A média é de solicitações 121/segundo.</p></li>
<li><p>Ao usar dois relatórios de servidor de relatório para o mesmo banco de dados do Microsoft SQL Server, as médias de solicitações/segundo são semelhantes a um único servidor de relatórios = ~ 127, com um máximo de solicitações 278 de/segundo.</p></li>
<li><p>Um único servidor de relatórios pode processar conexões simultâneas/ativas do 500.</p></li>
<li><p>Um único servidor de relatórios pode processar uma máxima conexão simultânea de 1500.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Banco de dados de relatório.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Bloquear a disputa no computador que executa o Microsoft SQL Server é o fator de limitação para solicitações/segundo.</p></li>
<li><p>A produtividade e o tempo de resposta são independentes do tamanho do banco de dados.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Calculando o atraso aleatório**:

O atraso aleatório especifica o atraso máximo (em minutos) dos dados a serem enviados para o servidor de relatórios. Quando a tarefa agendada for iniciada, o cliente gerará um atraso aleatório entre **0** e **ReportingRandomDelay** e esperará a duração especificada antes de enviar os dados.

Atraso aleatório = 4 \ * número de clientes/solicitações médias por segundo.

Exemplo: para clientes do 500, com solicitações do 120 por segundo, o atraso aleatório é, 4 \ * 500/120 = ~ 17 minutos.

## <a href="" id="---------app-v-5-0-publishing-server-capacity-planning-recommendations"></a> Recomendações de planejamento de capacidade do servidor de publicação do App-V 5,0


Os computadores que executam o cliente App-V 5,0 se conectam ao servidor de publicação do App-V 5,0 para enviar uma solicitação de atualização de publicação e receber uma resposta. O tempo de resposta de ida e volta é medido no computador que executa o cliente App-V 5,0. O tempo do processador é medido no servidor de publicação. Para obter mais informações sobre as configurações compatíveis do aplicativo de publicação do App-V 5,0, consulte [configurações compatíveis do App-v 5,0](app-v-50-supported-configurations.md).

**Importante**  A lista a seguir mostra os principais fatores a serem considerados ao configurar o servidor de publicação do App-V 5,0:

-   O número de clientes que se conectam simultaneamente a um único servidor de publicação.

-   O número de pacotes em cada atualização.

-   A largura de banda de rede disponível em seu ambiente entre o cliente e o servidor de publicação do App-V 5,0.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenário</th>
<th align="left">Resumo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Vários clientes do App-V 5,0 se conectam a um único servidor de publicação simultaneamente.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Um servidor de publicação com processadores dual core pode responder a no máximo 5000 clientes que solicitam uma atualização simultaneamente.</p></li>
<li><p>Para clientes do 5000-10000, o servidor de publicação requer um mínimo de quatro núcleos.</p></li>
<li><p>Para clientes do 10000-20000, o servidor de publicação deve ter núcleos de quatro processadores para tempos de resposta mais eficientes.</p></li>
<li><p>Um servidor de publicação com quad core pode atualizar até 10000 pacotes em 3 segundos. (Compatível com 10000 clientes simultâneos)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Número de pacotes em cada atualização.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>O aumento do número de pacotes aumentará o tempo de resposta em cerca de 40% (até 1000 pacotes).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Rede entre o cliente App-V 5,0 e o Publishing Server.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Em uma rede lenta (largura de banda de 1,5 Mbps), há um aumento de 97% no tempo de resposta em comparação com a LAN (até 1000 usuários).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Observação**  O uso da CPU do servidor de publicação sempre é alto durante o intervalo de tempo em que é preciso processar solicitações simultâneas ( &gt; 90% na maioria dos casos). O servidor de publicação pode manipular solicitações de cliente ~ 1500 em 1 segundo.

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenário</th>
<th align="left">Variação</th>
<th align="left">Número de clientes do App-V 5,0</th>
<th align="left">Número de pacotes</th>
<th align="left">Configuração do processador no servidor de publicação</th>
<th align="left">Servidor de publicação do tipo de conexão de rede/cliente do App-V 5,0</th>
<th align="left">Tempo de viagem de ida e volta no cliente do App-V 5,0 (em segundos)</th>
<th align="left">Utilização da CPU no servidor de publicação (em%)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 o cliente envia uma solicitação &amp; de atualização de publicação recebe resposta, cada solicitação contendo pacotes 120</p></td>
<td align="left"><p>Número de clientes</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>1000</p></li>
<li><p>5000</p></li>
<li><p>10000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Dual Core</p></li>
<li><p>Dual Core</p></li>
<li><p>Quad Core</p></li>
<li><p>Quad Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>um</p></li>
<li><p>2</p></li>
<li><p>2</p></li>
<li><p>3D</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>99</p></li>
<li><p>89</p></li>
<li><p>77</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Vários pacotes em cada atualização</p></td>
<td align="left"><p>Número de pacotes</p></td>
<td align="left"><p></p>
<ul>
<li><p>1000</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Quad Core</p></li>
<li><p>Quad Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>2</p></li>
<li><p>3D</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>92</p></li>
<li><p>91</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Rede entre o cliente e o servidor de publicação</p></td>
<td align="left"><p>rede de link lento de 1,5 Mbps</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Quad Core</p></li>
<li><p>Quad Core</p></li>
<li><p>Quad Core</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Rede intra-continental de 1,5 Mbps</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3D</p></li>
<li><p>10 (com taxa de falha de 0,2%)</p></li>
<li><p>17 (com uma taxa de falha de 1%)</p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-0-streaming-capacity-planning-recommendations"></a> Recomendações de planejamento de capacidade de streaming do App-V 5,0


Os computadores que executam o cliente App-V 5,0 transmitem o pacote de aplicativo virtual do servidor de streaming. O tempo de resposta de ida e volta é medido no computador que executa o cliente App-V 5,0 e é o tempo levado para transmitir todo o pacote.

**Importante**  A lista a seguir identifica os principais fatores a serem considerados ao configurar o servidor de streaming do App-V 5,0:

-   O número de pacotes de aplicativos de transmissão de clientes simultaneamente de um único servidor de streaming.

-   O tamanho do pacote que está sendo transmitido.

-   A largura de banda de rede disponível em seu ambiente entre o cliente e o servidor de streaming.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenário</th>
<th align="left">Resumo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Vários clientes do App-V 5,0 transmitem aplicativos de um único servidor de streaming simultaneamente.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Se o número de clientes que realizam streaming simultâneo do mesmo servidor aumentar, há uma relação linear com o tempo de download do pacote/tempo de streaming.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Tamanho do pacote que está sendo transmitido.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>O tamanho do pacote tem um impacto significativo no tempo de streaming/download apenas para pacotes maiores com um tamanho de aproximadamente 1GB. Para tamanhos de pacote entre 3 MB e 100 MB, o tempo de transmissão varia de 20 a 100 segundos a 100 clientes simultâneos.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Rede entre o cliente do App-V 5,0 e o servidor de streaming.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Em uma rede lenta (largura de banda de 1,5 Mbps), há um aumento de 70-80% no tempo de resposta em comparação com a LAN (até 100 usuários).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

A tabela a seguir exibe exemplos de valores para cada um dos fatores da lista anterior:

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
<th align="left">Cenário</th>
<th align="left">Variação</th>
<th align="left">Número de clientes do App-V 5,0</th>
<th align="left">Tamanho de cada pacote</th>
<th align="left">Cliente do tipo de conexão de rede Server/App-V 5,0</th>
<th align="left">Tempo de viagem de ida e volta no cliente do App-V 5,0 (em segundos)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Vários clientes do App-V 5,0 transmitindo pacotes de aplicativos virtuais de um servidor de fluxo contínuo.</p></td>
<td align="left"><p>Número de clientes.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 MB</p></li>
<li><p>3,5 MB</p></li>
<li><p>3,5 MB</p></li>
<li><p></p></li>
<li><p>5 MB</p></li>
<li><p>5 MB</p></li>
<li><p>5 MB</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>anos</p></li>
<li><p>39</p></li>
<li><p>391</p></li>
<li><p></p></li>
<li><p>35</p></li>
<li><p>68</p></li>
<li><p>461</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Tamanho de cada pacote que está sendo transmitido.</p></td>
<td align="left"><p>Tamanho de cada pacote.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>21 MB</p></li>
<li><p>21 MB</p></li>
<li><p></p></li>
<li><p>109</p></li>
<li><p>109</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<p>33</p>
<p>83</p>
<p></p>
<p>100</p>
<p>160</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conexão de rede entre o servidor de streaming do cliente e do App-V 5,0.</p></td>
<td align="left"><p>rede de link lento de 1,5 Mbps.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p></p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 MB</p></li>
<li><p></p></li>
<li><p>5 MB</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Rede intra-continental de 1,5 Mbps</p></li>
</ul></td>
<td align="left"><p></p>
<p>102</p>
<p></p>
<p>121</p></td>
</tr>
</tbody>
</table>

 

Cada servidor de streaming do App-V 5,0 deve ser capaz de manipular um mínimo de 200 clientes que transmitiram simultaneamente aplicativos virtualizados.

**Observação**  O tempo real para o fluxo será determinado principalmente pelo número de clientes que estão sendo transmitidos simultaneamente, número de pacotes, tamanho do pacote, atividade da rede do servidor e condições da rede.

 

Por exemplo, um usuário médio pode transmitir um pacote de 100 MB em menos de 2 minutos, quando 100 clientes simultâneos estão transmitindo do servidor. No entanto, um pacote de tamanho 1 GB pode levar até 30 minutos. Na maioria dos ambientes do mundo real, a demanda de transmissão não é distribuída de maneira uniforme, você precisará compreender os requisitos de streaming de pico aproximados presentes no ambiente para dimensionar corretamente o número de servidores de streaming necessários.

O número de clientes em que um servidor de streaming pode oferecer suporte pode ser aumentado significativamente e os requisitos de pico de streaming reduzidos se você armazenar previamente em cache seus aplicativos. Você também pode aumentar o número de clientes para o qual um servidor de streaming pode oferecer suporte usando pacotes otimizados sob demanda e pacotes otimizados de fluxo.

## Combinando funções de servidor do App-V 5,0


Com a descontamento dos requisitos de dimensionamento e tolerância a falhas, o número mínimo de servidores necessários para um local com conectividade com o Active Directory é um. Este servidor hospedará as funções servidor de gerenciamento, serviço servidor de gerenciamento e Microsoft SQL Server. As funções de servidor, portanto, podem ser organizadas em qualquer combinação desejada porque elas não entram em conflito umas com as outras.

Ignorar requisitos de dimensionamento, o número mínimo de servidores necessários para fornecer uma implementação tolerante a falhas é de quatro. O servidor de gerenciamento e as funções do Microsoft SQL Server dão suporte a serem colocadas em configurações tolerantes a falhas. O serviço do servidor de gerenciamento pode ser combinado com qualquer uma das funções, mas permanece um ponto único de falha.

Embora existam várias estratégias e tecnologias de tolerância a falhas disponíveis, nem todas são aplicáveis a um serviço específico. Além disso, se as funções do App-V 5,0 forem combinadas, algumas opções de tolerância a falhas não poderão mais se aplicar devido a incompatibilidades.






## Tópicos relacionados


[Configurações com suporte ao App-V 5.0](app-v-50-supported-configurations.md)

[Planejamento de alta disponibilidade com o App-V 5.0](planning-for-high-availability-with-app-v-50.md)

[Planejando a implantação do App-V](planning-to-deploy-app-v.md)

 

 





