---
title: Preparar uma implantação do UE-V 2. x
description: Preparar uma implantação do UE-V 2. x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799869"
---
# Preparar uma implantação do UE-V 2. x


Há algum planejamento e preparação antes de implantar o Microsoft User Experience Virtualization (UE-V) 2,0 ou 2,1 como uma solução para sincronizar as configurações entre dispositivos que os usuários acessam na sua empresa. Este tópico ajuda você a determinar o tipo de implantação que fará e qual será a preparação que você pode fazer de antemão para que sua implantação seja bem-sucedida.

Primeiro, vamos dar uma olhada nas tarefas que você vai fazer para implantar o UE-V:

-   Planejar a implantação do UE-V

    Antes de implantar qualquer coisa, uma boa primeira etapa é fazer um pouco de planejamento para que você possa determinar quais recursos do UE-V você vai implantar. Portanto, se você sair desta página, verifique se voltou e leu as informações de planejamento abaixo.

-   [Implantar os recursos necessários na UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Toda a implantação do UE-V requer estas atividades:

    -   [Definir um local de armazenamento de configurações](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Decidir como implantar o UE-V Agent e gerenciar as configurações de UE-V](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Instalar o UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) em cada computador do usuário que precisa de configurações sincronizadas

-   Opcionalmente, você pode [implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    O planejamento vai ajudá-lo a descobrir se você deseja que o UE-V ofereça suporte à sincronização de configurações para aplicativos personalizados (de terceiros ou de linha de negócios), o que exige estes recursos de UE-V:

    -   [Instale o gerador UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) para que você possa criar, editar e validar os modelos de local de configurações personalizadas necessários para sincronizar as configurações de aplicativo personalizadas

    -   [Criar modelos de local de configurações personalizadas](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) usando o UE-V Generator

    -   [Implantar um catálogo de modelos de configurações do UE-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) que você usa para armazenar seus modelos de local de configurações personalizadas

Este diagrama de fluxo de trabalho fornece uma compreensão de alto nível de uma implantação do UE-V e das decisões que determinam como você implanta o UE-V na sua empresa.

![deploymentworkflow](images/deploymentworkflow.png)

**Planejando uma implantação do UE-V:** Primeiro, você deseja fazer um pouco de planejamento para poder determinar quais componentes do UE-V você vai implantar. Planejar uma implantação do UE-V envolve estas coisas:

-   [Decida se deseja sincronizar as configurações para aplicativos personalizados](#deciding)

    Isso determina se você vai instalar o UE-V Generator durante a implantação, o que permite criar modelos de local de configurações personalizadas. Ele envolve o seguinte:

    Examine as [configurações que são sincronizadas automaticamente em uma implantação de UE-V](#autosyncsettings).

    [Determine se você precisa de configurações sincronizadas para outros aplicativos](#determinesettingssync).

-   Revise [outras considerações para a implantação do UE-V](#considerations), como alta disponibilidade e planejamento de capacidade.

-   [Confirme pré-requisitos e configurações com suporte para UE-V](#prereqs)

## <a href="" id="deciding"></a>Decida se deseja sincronizar as configurações para aplicativos personalizados


Em uma implantação do UE-V, muitas configurações são sincronizadas automaticamente. Mas você também pode personalizar o UE-V para sincronizar as configurações de outros aplicativos, como linha de negócios e aplicativos de terceiros.

Decidir se você deseja que o UE-V sincronize as configurações para aplicativos personalizados é provavelmente a parte mais importante de planejar sua implantação do UE-V. Os tópicos desta seção ajudarão você a tomar essa decisão.

### <a href="" id="autosyncsettings"></a>Configurações que são sincronizadas automaticamente em uma implantação do UE-V

Esta seção fornece informações sobre as configurações que são sincronizadas por padrão no UE-V, incluindo o seguinte:

Aplicativos da área de trabalho cujas configurações são sincronizadas por padrão

Configurações da área de trabalho do Windows que são sincronizadas por padrão

Uma declaração de suporte para a sincronização de configuração do aplicativo Windows

Consulte [modelos de configurações do User Experience Virtualization (UE-V) para que o Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) Baixe uma lista completa das configurações específicas do microsoft Office 2013, do microsoft Office 2010 e do microsoft Office 2007 que são sincronizadas por UE-V.

### Aplicativos da área de trabalho sincronizados por padrão no UE-V 2,1 e no UE-V 2,1 SP1

Quando você instala o agente do UE-V 2,1 ou do 2,1 SP1, ele registra um grupo padrão de modelos de local de configurações que capturam valores de configurações para esses aplicativos comuns da Microsoft.

**Dica**  
**Sincronização de configurações do Microsoft Office 2007** – no UE-V 2,1 e no 2,1 SP1, um modelo de local de configurações não é mais incluído por padrão para aplicativos do Office 2007. No entanto, você ainda pode usar os modelos do Office 2007 do UE-V 2,0 ou anterior e pode obter os modelos da [Galeria de modelos do UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoria do aplicativo</strong></th>
<th align="left"><strong>Descrição</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicativos do Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixar uma lista de todas as configurações sincronizadas </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicativos do Microsoft Office 2013</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixar uma lista de todas as configurações sincronizadas </a> )</p></td>
<td align="left"><p>Microsoft Word 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft Access 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Centro de carregamento do Microsoft Office 2013</p>
<p>Microsoft OneDrive for Business 2013</p>
<p>Os modelos de local de configurações do UE-V 2,1 e do 2,1 SP1 do Microsoft Office 2013 incluem suporte à assinatura aprimorada do Outlook. Adicionamos a sincronização das configurações de assinatura padrão para emails novos, de resposta e encaminhados.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Um perfil do Outlook deve ser criado para qualquer dispositivo no qual o usuário deseja sincronizar a assinatura do Outlook. Se o perfil ainda não tiver sido criado, o usuário poderá criar um e, em seguida, reiniciar o Outlook nesse dispositivo para habilitar a sincronização de assinatura.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Opções do navegador: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 e Internet Explorer 11</p></td>
<td align="left"><p>Favoritos, página inicial, guias e barras de ferramentas.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O UE-V não faz o roaming de configurações para cookies do Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Acessórios do Windows</p></td>
<td align="left"><p>Calculadora da Microsoft, bloco de notas, WordPad.</p></td>
</tr>
</tbody>
</table>



**Observação**  
O UE-V 2,1 SP1 não sincroniza as configurações entre a calculadora da Microsoft no Windows 10 e a calculadora da Microsoft em sistemas operacionais anteriores.



### Aplicativos da área de trabalho sincronizados por padrão no UE-V 2,0

Quando você instala o agente do UE-V 2,0, ele registra um grupo padrão de modelos de local de configurações que capturam valores de configurações para esses aplicativos comuns da Microsoft.

**Dica**  
**Sincronização de configurações do Microsoft Office 2013** – em UE-V 2,0, um modelo de local de configurações não é incluído por padrão para aplicativos do Office 2013, mas está disponível para download na [Galeria de modelos do UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589). A [sincronização do Office 2013 com o UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fornece detalhes sobre os modelos com suporte que sincronizam as configurações do Office 2013.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoria do aplicativo</strong></th>
<th align="left"><strong>Descrição</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicativos do Microsoft Office 2007</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixar uma lista de todas as configurações sincronizadas </a> )</p></td>
<td align="left"><p>Microsoft Access 2007</p>
<p>Microsoft Communicator 2007</p>
<p>Microsoft Excel 2007</p>
<p>Microsoft InfoPath 2007</p>
<p>Microsoft OneNote 2007</p>
<p>Microsoft Outlook 2007</p>
<p>Microsoft PowerPoint 2007</p>
<p>Microsoft Project 2007</p>
<p>Microsoft Publisher 2007</p>
<p>Microsoft SharePoint Designer 2007</p>
<p>Microsoft Visio 2007</p>
<p>Microsoft Word 2007</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicativos do Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixar uma lista de todas as configurações sincronizadas </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Opções do navegador: Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10</p></td>
<td align="left"><p>Favoritos, página inicial, guias e barras de ferramentas.</p>
<div class="alert">
<strong>Observação</strong><br/><p>O UE-V não faz o roaming de configurações para cookies do Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Acessórios do Windows</p></td>
<td align="left"><p>Calculadora da Microsoft, bloco de notas, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a>Configurações do Windows sincronizadas por padrão

O UE-V inclui modelos de local de configurações que capturam os valores das configurações do Windows.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">configurações do Windows</th>
<th align="left">Descrição</th>
<th align="left">Aplicar em</th>
<th align="left">Exportar em</th>
<th align="left">Estado padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tela de fundo da área de trabalho</p></td>
<td align="left"><p>Segundo plano ou papel de parede da área de trabalho ativa no momento.</p></td>
<td align="left"><p>Logon, desbloqueio, conexão remota, eventos de tarefa agendada.</p></td>
<td align="left"><p>Logoff, bloqueio, desconexão remota, usuário clicando em <strong> sincronizar agora </strong> no centro de configurações da empresa ou intervalo de tarefas agendadas</p></td>
<td align="left"><p>Habilitado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Facilidade de Acesso</p></td>
<td align="left"><p>Configurações de acessibilidade e de entrada, lente de opções da Microsoft, narrador e teclado virtual.</p></td>
<td align="left"><p>Somente logon.</p></td>
<td align="left"><p>Logoff, o usuário clica em <strong> sincronizar agora </strong> no centro de configurações da empresa ou no intervalo de tarefas agendadas</p></td>
<td align="left"><p>Habilitado</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações da área de trabalho</p></td>
<td align="left"><p>Menu iniciar e configurações da barra de tarefas, opções de pasta, ícones da área de trabalho padrão, relógios adicionais e configurações de região e idioma.</p></td>
<td align="left"><p>Somente logon.</p></td>
<td align="left"><p>Logoff, o usuário clica em <strong> sincronizar agora </strong> no centro de configurações da empresa ou em tarefa agendada</p></td>
<td align="left"><p>Habilitado</p></td>
</tr>
</tbody>
</table>



**Observação**  
A partir do Windows 8, o UE-V não faz a roaming de configurações relacionadas à tela inicial, como itens e locais. Além disso, o UE-V não dá suporte à sincronização de itens da barra de tarefas fixas ou atalhos de arquivos do Windows.



**Importante**  
As configurações de barra de tarefas de roaming do UE-V 2,1 SP1 entre dispositivos Windows 10. No entanto, o UE-V não sincroniza as configurações da barra de tarefas entre dispositivos Windows 10 e dispositivos que executam sistemas operacionais anteriores.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Grupo de configurações</th>
<th align="left">Categoria</th>
<th align="left">Chama</th>
<th align="left">Aplicar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configurações do aplicativo</strong></p></td>
<td align="left"><p>Aplicativos do Windows  </p></td>
<td align="left"><p>Fechar aplicativo</p>
<p>Evento de alteração das configurações do aplicativo do Windows</p></td>
<td align="left"><p>Iniciar o monitor do aplicativo UE-V na inicialização</p>
<p>Abrir o aplicativo</p>
<p>Evento de alteração das configurações do aplicativo do Windows</p>
<p>Chegada de um pacote de configurações</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Aplicativos da área de trabalho</p></td>
<td align="left"><p>Aplicativo é fechado</p></td>
<td align="left"><p>O aplicativo abre e fecha</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Configurações da área de trabalho</strong></p></td>
<td align="left"><p>Tela de fundo da área de trabalho</p></td>
<td align="left"><p>Bloquear ou fazer logoff</p></td>
<td align="left"><p>Logon, desbloqueio, conexão remota, notificação de Nova chegada de pacote, o usuário clica <strong> em sincronizar agora </strong> no centro de configurações da empresa ou quando a tarefa agendada é executada.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Facilidade de acesso (comum – acessibilidade, narrador, lupa, na tela-teclado)</p></td>
<td align="left"><p>Bloquear ou fazer logoff</p></td>
<td align="left"><p>Sessão</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Facilidade de acesso (shell-áudio, acessibilidade, teclado, mouse)</p></td>
<td align="left"><p>Bloquear ou fazer logoff</p></td>
<td align="left"><p>Logon, desbloqueio, conexão remota, notificação de Nova chegada de pacote, clicar em <strong> sincronizar agora </strong> no centro de configurações da empresa ou executar tarefas agendadas</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Configurações da área de trabalho</p></td>
<td align="left"><p>Bloquear ou fazer logoff</p></td>
<td align="left"><p>Sessão</p></td>
</tr>
</tbody>
</table>



### UE-V-suporte para aplicativos do Windows

Para aplicativos do Windows, o desenvolvedor do aplicativo especifica as configurações que são sincronizadas. Você pode especificar quais aplicativos do Windows estão habilitados para a sincronização de configurações.

Para exibir uma lista de aplicativos do Windows que podem sincronizar as configurações em um computador com o nome da família de pacotes, status habilitado e fonte habilitada, em um prompt de comando do Windows PowerShell, digite: `Get-UevAppxPackage`

**Observação**  
A partir do Windows 8, o UE-V não sincroniza as configurações do aplicativo do Windows se o usuário do domínio vincular suas credenciais de entrada à conta da Microsoft. Essa vinculação sincroniza as configurações do Microsoft OneDrive para UE-V, que desabilita a sincronização das configurações de aplicativo do Windows.



### UE-V-suporte para impressoras móveis

O UE-V 2,1 SP1 permite que impressoras de rede sejam movidas entre dispositivos para que um usuário tenha acesso às suas impressoras de rede quando estiver conectado a qualquer dispositivo na rede. Isso inclui o roaming da impressora definida como padrão.

O roaming da impressora no UE-V exige um dos seguintes cenários:

-   O servidor de impressão pode baixar o driver necessário quando ele está em roaming para um novo dispositivo.

-   O driver para a impressora de rede de roaming está pré-instalado em qualquer dispositivo que precise acessar a impressora de rede.

-   O driver da impressora pode ser obtido no Windows Update.

**Observação**  
O recurso de roaming da impressora UE-V **não transfere** preferências ou configurações de impressora, como impressão em frente e verso.



### <a href="" id="determinesettingssync"></a>Determinar se você precisa de configurações sincronizadas para outros aplicativos

Depois de revisar as configurações que são sincronizadas automaticamente em uma implantação do UE-V, você deseja decidir se sincronizará as configurações de outros aplicativos, pois determina como implantar o UE-V em toda a empresa.

Como administrador, quando você considera quais aplicativos da área de trabalho serão incluídos na sua solução UE-V, considere quais configurações podem ser personalizadas pelos usuários e como e onde o aplicativo armazena suas configurações. Nem todos os aplicativos da área de trabalho têm configurações que podem ser personalizadas ou que são rotineiramente personalizadas pelos usuários. Além disso, nem todas as configurações de aplicativos da área de trabalho podem ser sincronizadas com segurança em vários computadores ou ambientes.

Em geral, você pode sincronizar as configurações que atendem aos seguintes critérios:

-   Configurações armazenadas em locais acessíveis pelo usuário. Por exemplo, não sincronize as configurações armazenadas em system32 ou fora da seção HKEY \ _CURRENT \ _USER (HKCU) do registro.

-   Configurações que não são específicas do computador específico. Por exemplo, exclua configurações de rede ou de hardware.

-   Configurações que podem ser sincronizadas entre computadores sem risco de dados corrompidos. Por exemplo, não use configurações armazenadas em um arquivo de banco de dados.

### <a href="" id="checklistsettingssync"></a>Lista de verificação para avaliação de aplicativos personalizados

Se você tiver decidido que precisa de configurações sincronizadas para outros aplicativos, poderá usar esta lista de verificação para ajudar a descobrir quais aplicativos serão incluídos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Este aplicativo contém configurações que o usuário pode personalizar?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>É importante para o usuário que essas configurações são sincronizadas?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Essas configurações de usuário já são gerenciadas por uma solução de política de gerenciamento ou configurações de aplicativo? O UE-V aplica as configurações do aplicativo nas configurações de inicialização do aplicativo e do Windows durante eventos de logon, desbloqueio ou conexão remota. Se você usa o UE-V com outras soluções de compartilhamento de configurações, os usuários podem ter inconsistência nas configurações sincronizadas.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>As configurações do aplicativo são específicas do computador? Preferências de aplicativo e personalizações associadas a hardware ou configurações de computador específicas não sincronizam consistentemente entre as sessões e podem causar uma experiência de aplicativo ruim.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>As configurações da loja de aplicativos são encontradas no diretório arquivos de programas ou no diretório de arquivos localizado no diretório <strong> usuários </strong> [nome de usuário] &lt; Strong &gt; AppData </strong> &lt; Strong &gt; LocalLow </strong> ? Os dados de aplicativo armazenados em qualquer um desses locais normalmente não devem ser sincronizados com o usuário, pois esses dados são específicos do computador ou porque os dados são muito grandes para serem sincronizados.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>O aplicativo armazena todas as configurações em um arquivo que contém outros dados de aplicativo que não devem ser sincronizados? O UE-V sincroniza arquivos como uma unidade única. Se as configurações forem armazenadas em arquivos que incluam dados do aplicativo além das configurações, a sincronização desses dados adicionais poderá causar uma experiência de aplicativo deficiente.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Qual é o tamanho dos arquivos que contêm as configurações? O desempenho da sincronização de configurações pode ser afetado por arquivos grandes. Incluir arquivos grandes pode afetar o desempenho da sincronização das configurações.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a>Outras considerações ao preparar uma implantação de UE-V


Você também deve considerar essas coisas quando estiver se preparando para implantar o UE-V:

-   [Gerenciando a sincronização de credenciais](#creds)

-   [Sincronização de configurações do aplicativo do Windows](#appxsettings)

-   [Modelos de localização de configurações personalizadas de UE-V](#custom)

-   [Configurações de configurações do usuário não intencional](#prevent)

-   [Desempenho e capacidade](#capacity)

-   [Alta disponibilidade](#high)

-   [Sincronização do relógio do computador](#clocksync)

### <a href="" id="creds"></a>Gerenciando a sincronização de credenciais no UE-V 2,1 e no UE-V 2,1 SP1

Muitos aplicativos corporativos, incluindo o Microsoft Outlook e o Lync, solicitam aos usuários suas credenciais de domínio ao fazer logon. Os usuários têm a opção de salvar as credenciais em disco para evitar que você precise digitá-las toda vez que abrirem esses aplicativos. Habilitar a sincronização de credenciais de roaming permite que os usuários salvem suas credenciais em um computador e evite digitá-las novamente em cada computador usado em seu ambiente. Os usuários podem sincronizar algumas credenciais de domínio com o UE-V 2,1 e o 2,1 SP1.

**Importante**  
A sincronização de credenciais é desativada por padrão. Você deve habilitar explicitamente a sincronização de credenciais durante a implantação para implementar esse recurso.



O UE-V 2,1 e o 2,1 SP1 podem sincronizar as credenciais da empresa, mas não use o roaming de credenciais somente para uso no computador local.

As credenciais são configurações síncronas, o que significa que elas são aplicadas ao seu perfil na primeira vez que você se conecta ao computador após a sincronização do UE-V.

A sincronização de credenciais é gerenciada por seu próprio modelo de local de configurações, que é desabilitado por padrão. Você pode habilitar ou desabilitar esse modelo por meio dos mesmos métodos usados para outros modelos. O identificador de modelo para esse recurso é RoamingCredentialSettings.

**Importante**  
Se você estiver usando o roaming de credenciais do Active Directory em seu ambiente, recomendamos que você não habilite o modelo de roaming de credenciais do UE-V.



Use um destes métodos para habilitar a sincronização de credenciais:

-   Centro de configurações da empresa

-   PowerShell

-   Política de Grupo

**Observação**  
As credenciais são criptografadas durante a sincronização.



[Centro de configurações da empresa](https://technet.microsoft.com/library/dn458903.aspx)**:** marque a caixa de seleção configurações de credenciais de roaming em configurações do Windows para habilitar a sincronização de credenciais. Desmarque a caixa para desabilitá-la. Essa caixa de seleção aparecerá apenas na central de configurações da empresa se a sua conta não estiver configurada para sincronizar as configurações usando uma conta da Microsoft.

[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** este cmdlet do PowerShell permite a sincronização de credenciais:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Este cmdlet do PowerShell desabilita a sincronização de credenciais:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Política de grupo](https://technet.microsoft.com/library/dn458893.aspx)**:** você deve [implantar o modelo ADMX mais recente do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) para habilitar a sincronização de credenciais por meio da política de grupo. A sincronização de credenciais é gerenciada com as configurações do Windows. Para gerenciar esse recurso com a política de grupo, habilite a política sincronizar configurações do Windows.

1.  Abra o editor de política de grupo e navegue até **configuração do usuário – modelos administrativos – componentes do Windows – virtualização da experiência do usuário da Microsoft**.

2.  Clique duas vezes em **sincronizar configurações do Windows**.

3.  Se essa política estiver habilitada, você poderá habilitar a sincronização de credenciais marcando a caixa de seleção **credenciais de roaming** ou desabilitar a sincronização de credenciais desmarcando-a.

4.  Clique em **OK**.

### Locais de credenciais sincronizados pela UE-V

Os arquivos de credenciais salvos por aplicativos nos seguintes locais são sincronizados:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

As credenciais salvas em outros locais não são sincronizadas pela UE-V.

### <a href="" id="appxsettings"></a>Sincronização de configurações do aplicativo do Windows

O UE-V gerencia a sincronização das configurações do aplicativo Windows de três maneiras:

-   **Sincronizar aplicativos do Windows:** Permitir ou negar a sincronização de qualquer aplicativo do Windows

-   **Lista de aplicativos do Windows:** Sincronizar uma lista de aplicativos do Windows

-   **Comportamento de sincronização padrão não listado:** Determine o comportamento de sincronização dos aplicativos do Windows que não estão na lista de aplicativos do Windows.

Para obter mais informações, consulte a [lista de aplicativos do Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

### <a href="" id="custom"></a>Modelos de localização de configurações personalizadas de UE-V

Se você estiver implantando o UE-V para sincronizar as configurações de aplicativos personalizados, usará o UE-V Generator para criar modelos de localização de configurações personalizadas para esses aplicativos da área de trabalho. Depois de criar e testar um modelo de local de configurações personalizado em um ambiente de teste, você pode implantar os modelos de local de configurações em computadores na empresa.

Modelos de localização de configurações personalizadas devem ser implantados com uma infraestrutura de implantação existente, como um método ESD (Enterprise Software Distribution), como o System Center Configuration Manager, com preferências ou configurando um catálogo de modelos de configurações do UE-V. Os modelos implantados com o Configuration Manager ou a política de grupo devem ser registrados usando o UE-V WMI ou o Windows PowerShell.

Para obter mais informações sobre modelos de localização de configurações personalizadas, consulte [implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Para obter mais informações sobre como usar o UE-V com o Configuration Manager, consulte [Configurando o UE-v 2. x com o System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

### <a href="" id="prevent"></a>Impedir a configuração de configurações do usuário não intencional

O UE-V baixa as informações de novas configurações de usuário de um local de armazenamento de configurações e aplica as configurações ao computador local nestes casos:

-   Toda vez que um aplicativo é iniciado com um modelo UE-V registrado.

-   Quando um usuário faz logon em um computador.

-   Quando um usuário desbloqueia um computador.

-   Quando é feita uma conexão com um computador de área de trabalho remota com UE-V instalado.

-   Quando a tarefa agendada do aplicativo de controlador de sincronização estiver em execução.

Se o UE-V estiver instalado no computador A e no computador B e as configurações desejadas para o aplicativo estiverem no computador A, o computador A deve abrir e fechar o aplicativo primeiro. Se o aplicativo for aberto e fechado no computador B primeiro, as configurações do aplicativo no computador A serão configuradas para as configurações do aplicativo no computador B. as configurações são sincronizadas entre computadores em cada aplicativo. Com o passar do tempo, as configurações ficam consistentes entre computadores à medida que eles são abertos e fechados com configurações preferenciais.

Esse cenário também se aplica às configurações do Windows. Se as configurações do Windows no computador B devem ser iguais às do Windows no computador A, o usuário deve fazer logon e fazer logoff do computador A primeiro.

Se as configurações do usuário que o usuário quer forem aplicadas na ordem errada, elas poderão ser recuperadas ao executar uma operação de restauração para o aplicativo específico ou a configuração do Windows no computador em que as configurações foram sobrescritas. Para obter mais informações, consulte [gerenciar backup e restauração administrativos no UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a href="" id="capacity"></a>Desempenho e planejamento de capacidade

Especifique seus requisitos para UE-V com capacidade de disco padrão e monitoramento da integridade da rede.

O UE-V usa um compartilhamento SMB (Server Message Block) para o armazenamento de pacotes de configurações. O tamanho dos pacotes de configurações varia de acordo com as informações de configuração de cada aplicativo. Embora a maioria dos pacotes de configurações seja pequena, a sincronização de arquivos potencialmente grandes, como imagens da área de trabalho, pode resultar em desempenho ruim, principalmente em redes mais lentas.

Para reduzir problemas com a latência da rede, crie locais de armazenamento de configurações nas mesmas redes locais em que os computadores dos usuários residem. Recomendamos 20 MB de espaço em disco por usuário para o local de armazenamento de configurações.

Por padrão, a sincronização do UE-V expira após 2 segundos para evitar retardo excessivo devido a um pacote de configurações grande. Você pode configurar a configuração SyncMethod = SyncProvider usando [objetos de política de grupo](https://technet.microsoft.com/library/dn458893.aspx).

### <a href="" id="high"></a>Alta disponibilidade para UE-V

O catálogo de modelos de configurações e local de armazenamento de configurações do UE-V dão suporte ao armazenamento de dados do usuário em qualquer compartilhamento gravável. Para garantir alta disponibilidade, siga estes critérios:

-   Formate o volume de armazenamento com um sistema de arquivos NTFS.

-   O compartilhamento pode usar o sistema de arquivos distribuídos (DFS), mas há restrições.
Especificamente, não há suporte para a configuração de destino único DFS-R (DFS – Distributed File System Replication) com ou sem um namespace do sistema de arquivos distribuído (DFS-N).
Da mesma forma, somente a configuração de destino única é compatível com o DFS-N.
Para obter informações detalhadas, consulte a [declaração de suporte da Microsoft em torno de dados de perfil de usuário replicado](https://go.microsoft.com/fwlink/p/?LinkId=313991) e também [informações sobre a política de suporte da Microsoft para um cenário de implantação DFS-R e DFS-N](https://support.microsoft.com/kb/2533009).

    Além disso, como o SYSVOL usa o DFS-R para replicação, o SYSVOL não pode ser usado para a replicação de arquivos de dados do UE-V.

-   Configure as permissões de compartilhamento e as listas de controle de acesso NTFS (ACLs) conforme especificado em [implantando o local de armazenamento de configurações para UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Use o agrupamento de servidor de arquivos juntamente com o UE-V Agent para fornecer acesso a cópias de dados de estado do usuário no caso de falhas de comunicação.

-   Você pode armazenar os dados de caminho de armazenamento de configurações (dados do usuário) e modelos de catálogo de modelos de configurações em compartilhamentos de cluster, em compartilhamentos DFS-N ou em ambos.

### <a href="" id="clocksync"></a>Sincronizar os relógios do computador para a sincronização de configurações do UE-V

Os computadores que executam o UE-V Agent devem usar um servidor de horário para manter uma experiência de configuração consistente. O UE-V usa carimbos de data/hora para determinar se as configurações devem ser sincronizadas do local de armazenamento de configurações. Se o relógio do computador não for exato, as configurações mais antigas podem substituir as configurações mais recentes, ou as novas configurações podem não ser salvas no local de armazenamento de configurações.

## <a href="" id="prereqs"></a>Confirme pré-requisitos e configurações com suporte para UE-V


Antes de prosseguir, verifique se o seu ambiente inclui estes requisitos para executar o UE-V.

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
<th align="left"><strong>Sistema operacional</strong></th>
<th align="left"><strong>Edição</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Arquitetura do sistema</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Ultimate, Enterprise ou Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5 ou superior para UE-V 2,1.</p>
<p>.NET Framework 4 ou superior para UE-V 2,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter ou servidor Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5 ou superior para UE-V 2,1.</p>
<p>.NET Framework 4 ou superior para UE-V 2,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 e Windows 8,1</p></td>
<td align="left"><p>Enterprise ou pro</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5 ou superior</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, versão anterior ao 1607</p>
<div class="alert">
<strong>Observação</strong><br/><p>Somente o UE-V 2,1 SP1 é compatível com o Windows 10, versão anterior ao 1607</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise ou pro</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 e Windows Server 2012 R2</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5 ou superior</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,6 ou superior</p></td>
</tr>
</tbody>
</table>



Também...

-   **Licença do MDOP:** Essa tecnologia é parte do Microsoft Desktop Optimization Pack (MDOP). Os clientes empresariais podem obter o MDOP com o Microsoft Software Assurance. Para obter mais informações sobre o Microsoft Software Assurance e sobre como adquirir o MDOP, consulte como obter o MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Credenciais administrativas** para qualquer computador no qual você irá instalar

**Observação**  

-   A partir do WIndows 10, versão 1607, o UE-V está incluído no [Windows 10 para empresas](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e não faz mais parte do Microsoft Desktop Optimization Pack.

-   O recurso do UE-V Windows PowerShell do UE-V Agent requer o .NET Framework 4 ou superior, e o Windows PowerShell 3,0 ou superior esteja habilitado. Baixe o Windows PowerShell 3,0 [aqui](https://go.microsoft.com/fwlink/?LinkId=309609).

-   Instale o .NET Framework 4 ou o .NET Framework 4,5 em computadores que executam o sistema operacional Windows 7 ou Windows Server 2008 R2. Os sistemas operacionais Windows 8, Windows 8,1 e Windows Server 2012 vêm com o .NET Framework 4,5 instalado. O sistema operacional Windows 10 vem com o .NET Framework 4,6 instalado.
-   A política "Excluir cache de roaming" para perfis obrigatórios não é compatível com UE-V e não deve ser usada.



Não há requisitos especiais de memória de acesso aleatório (RAM) específicos para o UE-V.

### Sincronização de configurações por meio do provedor de sincronização

O provedor de sincronização é a configuração padrão para os usuários, que sincroniza um cache local com o local de armazenamento de configurações nestes casos:

-   Logon/logoff

-   Bloquear/desbloquear

-   Conexão/desconexão da área de trabalho remota

-   Abrir/fechar aplicativo

Uma tarefa agendada gerencia essa sincronização de configurações a cada 30 minutos ou por meio de certos eventos de gatilho para determinados aplicativos. Para obter mais informações, consulte [alterando a frequência das tarefas agendadas de UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

O UE-V Agent sincroniza as configurações do usuário para computadores que não estão sempre conectados à rede corporativa (computadores remotos e laptops) e computadores que estão sempre conectados à rede (computadores que executam o Windows Server e hospedam sessões da interface de área de trabalho virtual (VDI)).

**Sincronização para computadores com conexões sempre disponíveis:** Quando você usa o UE-V em computadores que estão sempre conectados à rede, você deve configurar o UE-V Agent para sincronizar as configurações usando o parâmetro *SyncMethod = None* , que trata o servidor de armazenamento de configurações como um compartilhamento de rede padrão. Nesta configuração, o UE-V Agent pode ser configurado para notificar se a importação das configurações do aplicativo for adiada.

Habilite essa configuração por meio de um destes métodos:

-   Durante a instalação do UE-V, no prompt de comando ou em um arquivo em lotes, defina o parâmetro AgentSetup.exe *SyncMethod = None*. [A implantação do agente do UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) fornece mais informações.

-   Após a instalação do UE-V, use o recurso de gerenciamento de configurações no System Center 2012 Configuration Manager ou os modelos ADMX do MDOP para empurrar a configuração *SyncMethod = None* .

-   Use o Windows PowerShell ou WMI (Instrumentação de gerenciamento do Windows) para definir a configuração *SyncMethod = None* .

    **Observação**  
    Esses dois últimos métodos não funcionam para ambientes de infraestrutura de área de trabalho virtual (VDI) em pool.



Você deve reiniciar o computador para que as configurações comecem a sincronizar.

**Observação**  
Se você definir *SyncMethod = None*, todas as alterações de configurações serão salvas diretamente no servidor. Se a conexão de rede com o caminho de armazenamento de configurações não for encontrada, as alterações de configurações serão armazenadas em cache no dispositivo e sincronizadas na próxima vez que o provedor de sincronização for executado. Se o caminho de armazenamento de configurações não for encontrado e o perfil do usuário for removido de um ambiente de VDI em pool no logoff, as alterações de configurações serão perdidas e o usuário deverá reaplicar a alteração quando o computador for reconectado ao caminho de armazenamento de configurações.



**Sincronização para mecanismos de sincronização externos:** O parâmetro *SyncMethod = external* especifica que se as configurações de UE-V forem gravadas em uma pasta local no computador do usuário, qualquer mecanismo de sincronização externo (como o onedrive for Business, as pastas de trabalho, o SharePoint ou o Dropbox) pode ser usado para aplicar essas configurações aos diferentes computadores que os usuários acessam.

**Suporte para sessões de VDI compartilhadas:** O UE-V 2,1 e o 2,1 SP1 oferecem suporte a sessões do VDI compartilhadas entre os usuários finais. Você pode registrar e configurar um modelo VDI especial, o que garante que o UE-V mantém toda a funcionalidade intacta em sessões de VDI não persistentes.

**Observação**  
Se você não habilitar o modo VDI para sessões de VDI não persistentes, alguns recursos não funcionarão, como [backup/restauração e última configuração válida (LKG)](https://technet.microsoft.com/library/dn878331.aspx).



O modelo VDI é fornecido com o UE-V 2,1 e o 2,1 SP1 e geralmente está disponível aqui após a instalação: C:\\Arquivos de experiência do usuário do Files\\Microsoft Virtualization\\Templates\\VdiState.xml

### Pré-requisitos para suporte ao gerador do UE-V

Instale o UE-V Generator no computador que é usado para criar modelos de local de configurações personalizadas. Este computador deve poder executar os aplicativos cujas configurações são sincronizadas. Você deve ser membro do grupo Administradores no computador que executa o software do gerador do UE-V.

O UE-V Generator deve ser instalado em um computador que usa um sistema de arquivos NTFS. O software do gerador do UE-V requer o .NET Framework 4. Para obter mais informações, consulte [implantar o UE-V 2. x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## Outros recursos para este produto


-   [Microsoft User Experience Virtualization (UE-V) 2. x](index.md)

-   [Introdução ao UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Solução de problemas do UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














