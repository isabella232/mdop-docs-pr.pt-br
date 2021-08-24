---
title: Preparar uma implantação UE-V 2.x
description: Preparar uma implantação UE-V 2.x
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
ms.openlocfilehash: 3e4d4b69975deda473372345733d8e8593a4775d
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910526"
---
# <a name="prepare-a-ue-v-2x-deployment"></a>Preparar uma implantação UE-V 2.x


Há algum planejamento e preparação a fazer antes de implantar o Microsoft User Experience Virtualization (UE-V) 2.0 ou 2.1 como uma solução para sincronizar configurações entre dispositivos que os usuários acessam em sua empresa. Este tópico ajuda você a determinar que tipo de implantação você fará e qual preparação você pode preparar antecipadamente para que sua implantação seja bem-sucedida.

Primeiro, vamos ver as tarefas que você fará para implantar UE-V:

-   Planejar sua implantação UE-V de usuário

    Antes de implantar qualquer coisa, uma boa primeira etapa é fazer um pouco de planejamento para que você possa determinar quais recursos UE-V você implantará. Portanto, se você sair desta página, certifique-se de voltar e ler as informações de planejamento abaixo.

-   [Implantar os recursos necessários na UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Cada UE-V de implantação requer estas atividades:

    -   [Definir um local de armazenamento de configurações](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Decidir como implantar o agente UE-V e gerenciar UE-V configurações](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Instalar o UE-V em](https://technet.microsoft.com/library/dn458891.aspx#agent) todos os computadores de usuário que precisem de configurações sincronizadas

-   Opcionalmente, você pode [implantar o UE-V 2.x para aplicativos personalizados](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    O planejamento ajudará você a descobrir se você deseja UE-V a sincronização de configurações para aplicativos personalizados (terceiros ou linha de negócios), o que exige esses recursos UE-V:

    -   [Instale o Gerador UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) para que você possa criar, editar e validar os modelos de local de configurações personalizadas necessários para sincronizar as configurações personalizadas do aplicativo

    -   [Criar modelos de localização de configurações personalizadas](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) usando o UE-V Generator

    -   [Implantar um UE-V de modelos](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) de configurações que você usa para armazenar seus modelos de localização de configurações personalizadas

Este diagrama de fluxo de trabalho fornece uma compreensão de alto nível de uma implantação UE-V e as decisões que determinam como você UE-V em sua empresa.

![deploymentworkflow.](images/deploymentworkflow.png)

**Planejando uma implantação UE-V:** Primeiro, você deseja fazer um pouco de planejamento para que possa determinar quais componentes UE-V você vai implantar. Planejar uma implantação UE-V envolve estas coisas:

-   [Decidir se é preciso sincronizar configurações para aplicativos personalizados](#deciding)

    Isso determina se você instalará o gerador UE-V durante a implantação, o que permite criar modelos de local de configurações personalizadas. Envolve o seguinte:

    Revise as [configurações sincronizadas automaticamente em uma implantação UE-V .](#autosyncsettings)

    [Determine se você precisa de configurações sincronizadas para outros aplicativos.](#determinesettingssync)

-   Revise [outras considerações sobre como implantar UE-V](#considerations), como planejamento de alta disponibilidade e capacidade.

-   [Confirmar pré-requisitos e configurações com suporte para UE-V](#prereqs)

## <a name="decide-whether-to-synchronize-settings-for-custom-applications"></a><a href="" id="deciding"></a>Decidir se deve sincronizar Configurações aplicativos personalizados


Em uma implantação UE-V, muitas configurações são sincronizadas automaticamente. Mas você também pode personalizar UE-V para sincronizar configurações para outros aplicativos, como aplicativos de linha de negócios e de terceiros.

Decidir se você deseja UE-V sincronizar configurações para aplicativos personalizados provavelmente é a parte mais importante do planejamento de sua implantação UE-V. Os tópicos desta seção ajudarão você a tomar essa decisão.

### <a name="settings-that-are-automatically-synchronized-in-a-ue-v-deployment"></a><a href="" id="autosyncsettings"></a>Configurações sincronizados automaticamente em uma implantação UE-V de dados

Esta seção fornece informações sobre as configurações sincronizadas por padrão no UE-V, incluindo o seguinte:

Aplicativos de área de trabalho cujas configurações são sincronizadas por padrão

Windows da área de trabalho sincronizadas por padrão

Uma instrução de suporte para Windows sincronização de configuração de aplicativo

Confira Modelos de configurações de Virtualização da Experiência do Usuário [(UE-V)](https://www.microsoft.com/download/details.aspx?id=46367) para Microsoft Office baixar uma lista completa das configurações específicas do Microsoft Office 2013, Microsoft Office 2010 e Microsoft Office 2007 que são sincronizadas pelo UE-V.

### <a name="desktop-applications-synchronized-by-default-in-ue-v-21-and-ue-v-21-sp1"></a>Aplicativos de área de trabalho sincronizados por padrão UE-V 2.1 e UE-V 2.1 SP1

Quando você instala o UE-V 2.1 ou 2.1 SP1 Agent, ele registra um grupo padrão de modelos de localização de configurações que capturam valores de configurações para esses aplicativos Comuns da Microsoft.

**Dica**  
**Microsoft Office 2007 Configurações Sincronização** – no UE-V 2.1 e 2.1 SP1, um modelo de local de configurações não é mais incluído por padrão para aplicativos Office 2007. No entanto, você ainda pode usar Office modelos 2007 UE-V 2.0 ou anteriores e pode obter os modelos da galeria de modelos [UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589).



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoria de aplicativo</strong></th>
<th align="left"><strong>Descrição</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Office aplicativos 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixe uma lista de todas as configurações sincronizadas </a> )</p></td>
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
<td align="left"><p>Microsoft Office 2013</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixe uma lista de todas as configurações sincronizadas </a> )</p></td>
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
<p>Microsoft Office 2013 Upload Center</p>
<p>Microsoft OneDrive para Empresas 2013</p>
<p>Os UE-V de configurações 2.1 e 2.1 SP1 Microsoft Office 2013 incluem suporte Outlook assinatura aprimorado. Adicionamos a sincronização de configurações de assinatura padrão para emails novos, de resposta e encaminhados.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Um Outlook perfil deve ser criado para qualquer dispositivo no qual um usuário queira sincronizar sua assinatura Outlook. Se o perfil ainda não tiver sido criado, o usuário poderá criar um e reiniciar Outlook nesse dispositivo para habilitar a sincronização de assinatura.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Opções do navegador: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 e Internet Explorer 11</p></td>
<td align="left"><p>Favoritos, home page, guias e barras de ferramentas.</p>
<div class="alert">
<strong>Observação</strong><br/><p>UE-V configurações de roam para cookies do Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows acessórios</p></td>
<td align="left"><p>Calculadora Microsoft, Bloco de notas, WordPad.</p></td>
</tr>
</tbody>
</table>



**Observação**  
UE-V 2.1 SP1 não sincroniza configurações entre o Calculadora Microsoft no Windows 10 e o Calculadora Microsoft em sistemas operacionais anteriores.



### <a name="desktop-applications-synchronized-by-default-in-ue-v-20"></a>Aplicativos de área de trabalho sincronizados por padrão UE-V 2.0

Quando você instala o UE-V 2.0 Agent, ele registra um grupo padrão de modelos de localização de configurações que capturam valores de configurações para esses aplicativos Comuns da Microsoft.

**Dica**  
**Microsoft Office 2013 Configurações Sincronização** – No UE-V 2.0, um modelo de local de configurações não é incluído por padrão para aplicativos do Office 2013, mas está disponível para download na galeria de modelos [do UE-V.](https://go.microsoft.com/fwlink/p/?LinkID=246589) [A sincronização Office 2013 com o UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fornece detalhes sobre os modelos com suporte que sincronizam as configurações Office 2013.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoria de aplicativo</strong></th>
<th align="left"><strong>Descrição</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Office aplicativos 2007</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixe uma lista de todas as configurações sincronizadas </a> )</p></td>
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
<td align="left"><p>Microsoft Office aplicativos 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Baixe uma lista de todas as configurações sincronizadas </a> )</p></td>
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
<td align="left"><p>Favoritos, home page, guias e barras de ferramentas.</p>
<div class="alert">
<strong>Observação</strong><br/><p>UE-V configurações de roam para cookies do Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows acessórios</p></td>
<td align="left"><p>Calculadora Microsoft, Bloco de notas, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a name="windows-settings-synchronized-by-default"></a><a href="" id="autosyncsettings2"></a>Windows configurações sincronizadas por padrão

UE-V inclui modelos de localização de configurações que capturam valores de configurações para essas Windows configurações.

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
<td align="left"><p>Plano de fundo ou papel de parede da área de trabalho ativo no momento.</p></td>
<td align="left"><p>Logon, desbloqueio, conexão remota, eventos de Tarefa Agendada.</p></td>
<td align="left"><p>Logoff, bloqueio, desconexão remota, usuário clicando em Sincronizar Agora no Centro de Configurações da empresa <strong> ou intervalo de tarefas </strong> agendados</p></td>
<td align="left"><p>Habilitada</p></td>
</tr>
<tr class="even">
<td align="left"><p>Facilidade de Acesso</p></td>
<td align="left"><p>Configurações de acessibilidade e entrada, Lupa da Microsoft, Narrador e teclado na tela.</p></td>
<td align="left"><p>Somente logon.</p></td>
<td align="left"><p>Logoff, usuário clicando em Sincronizar Agora no Centro Configurações <strong> empresa ou intervalo de tarefas </strong> agendados</p></td>
<td align="left"><p>Habilitada</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações da área de trabalho</p></td>
<td align="left"><p>menu Iniciar e configurações da barra de tarefas, opções de pasta, ícones de área de trabalho padrão, relógios adicionais e configurações de Região e Idioma.</p></td>
<td align="left"><p>Somente logon.</p></td>
<td align="left"><p>Logoff, usuário clicando em Sincronizar Agora no Centro Configurações <strong> Empresa ou tarefa </strong> agendada</p></td>
<td align="left"><p>Habilitada</p></td>
</tr>
</tbody>
</table>



**Observação**  
A partir Windows 8, UE-V configurações de roam não relacionadas à tela Inicial, como itens e locais. Além disso, UE-V não dá suporte à sincronização de itens de barra de tarefas fixados ou Windows atalhos de arquivo.



**Importante**  
UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices. No entanto, UE-V não sincroniza as configurações da barra de tarefas entre Windows 10 dispositivos que executam sistemas operacionais anteriores.



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
<th align="left">Captura</th>
<th align="left">Aplicar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Aplicativo Configurações</strong></p></td>
<td align="left"><p>Aplicativos do Windows  </p></td>
<td align="left"><p>Fechar aplicativo</p>
<p>Windows de configurações do aplicativo mudam o evento</p></td>
<td align="left"><p>Iniciar o UE-V de aplicativos na inicialização</p>
<p>Abrir aplicativo</p>
<p>Windows Evento Configurações alteração de aplicativo</p>
<p>Chegada de um pacote de configurações</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Aplicativos da área de trabalho</p></td>
<td align="left"><p>O aplicativo é fechado</p></td>
<td align="left"><p>Aplicativo abre e fecha</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Configurações da área de trabalho</strong></p></td>
<td align="left"><p>Tela de fundo da área de trabalho</p></td>
<td align="left"><p>Bloqueio ou logoff</p></td>
<td align="left"><p>Logon, desbloqueio, conexão remota, notificação da chegada do novo pacote, o usuário clica em Sincronizar Agora no Centro de Configurações empresa ou em tarefas <strong> </strong> agendadas.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Facilidade de acesso (Comum – Acessibilidade, Narrador, Lupa, Teclado na Tela)</p></td>
<td align="left"><p>Bloqueio ou Logoff</p></td>
<td align="left"><p>Logon</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Facilidade de acesso (Shell - Áudio, Acessibilidade, Teclado, Mouse)</p></td>
<td align="left"><p>Bloqueio ou logoff</p></td>
<td align="left"><p>Logon, desbloqueio, conexão remota, notificação da chegada do novo pacote, clique em Sincronizar Agora no Centro de Configurações Empresa ou em tarefas <strong> </strong> agendadas</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Configurações da área de trabalho</p></td>
<td align="left"><p>Bloqueio ou logoff</p></td>
<td align="left"><p>Logon</p></td>
</tr>
</tbody>
</table>



### <a name="ue-v-support-for-windows-apps"></a>UE-V suporte para aplicativos Windows aplicativos

Para Windows aplicativos, o desenvolvedor do aplicativo especifica as configurações sincronizadas. Você pode especificar quais Windows aplicativos estão habilitados para sincronização de configurações.

Para exibir uma lista de aplicativos Windows que podem sincronizar as configurações em um computador com o nome da família de pacotes, o status habilitado e a origem habilitada, em um prompt de comando Windows PowerShell, digite: `Get-UevAppxPackage`

**Observação**  
A partir Windows 8, o UE-V não sincroniza as configurações do aplicativo Windows se o usuário do domínio vincular suas credenciais de login à conta da Microsoft. Essa vinculação sincroniza as configurações para Microsoft OneDrive para UE-V, o que desabilita a sincronização de Windows configurações do aplicativo.



### <a name="ue-v-support-for-roaming-printers"></a>UE-V suporte para impressoras roaming

UE-V 2.1 SP1 permite que as impressoras de rede percoram entre dispositivos para que um usuário tenha acesso às impressoras de rede quando conectado a qualquer dispositivo na rede. Isso inclui o roaming da impressora definida como padrão.

O roaming de impressora UE-V requer um destes cenários:

-   O servidor de impressão pode baixar o driver necessário quando ele circula para um novo dispositivo.

-   O driver da impressora de rede móvel é pré-instalado em qualquer dispositivo que precise acessar essa impressora de rede.

-   O driver de impressora pode ser obtido do Windows Update.

**Observação**  
O UE-V de roaming de impressora **não** circula as configurações ou preferências da impressora, como a impressão de lado duplo.



### <a name="determine-whether-you-need-settings-synchronized-for-other-applications"></a><a href="" id="determinesettingssync"></a>Determinar se você precisa de configurações sincronizadas para outros aplicativos

Depois de revisar as configurações sincronizadas automaticamente em uma implantação UE-V, você deseja decidir se sincroniza as configurações para outros aplicativos, pois isso determina como implantar o UE-V em toda a sua empresa.

Como administrador, ao considerar quais aplicativos de área de trabalho incluir na sua solução de UE-V, considere quais configurações podem ser personalizadas pelos usuários e como e onde o aplicativo armazena suas configurações. Nem todos os aplicativos da área de trabalho têm configurações que podem ser personalizadas ou que são personalizadas rotineiramente pelos usuários. Além disso, nem todas as configurações de aplicativos de área de trabalho podem ser sincronizadas com segurança em vários computadores ou ambientes.

Em geral, você pode sincronizar configurações que atendem aos seguintes critérios:

-   Configurações que são armazenados em locais acessíveis ao usuário. Por exemplo, não sincronizar as configurações armazenadas no System32 ou fora da seção HKEY\_CURRENT\_USER (HKCU) do Registro.

-   Configurações que não são específicos para o computador específico. Por exemplo, exclua configurações de rede ou hardware.

-   Configurações que podem ser sincronizados entre computadores sem risco de dados corrompidos. Por exemplo, não use configurações armazenadas em um arquivo de banco de dados.

### <a name="checklist-for-evaluating-custom-applications"></a><a href="" id="checklistsettingssync"></a>Lista de verificação para avaliar aplicativos personalizados

Se você decidiu que precisa de configurações sincronizadas para outros aplicativos, você pode usar essa lista de verificação para ajudar a descobrir quais aplicativos você incluirá.

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
<td align="left"><p>Esse aplicativo contém configurações que o usuário pode personalizar?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>É importante para o usuário que essas configurações sejam sincronizadas?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Essas configurações de usuário já são gerenciadas por uma solução de política de gerenciamento de aplicativos ou configurações? UE-V aplica configurações de aplicativo na inicialização do aplicativo e Windows configurações em eventos de logon, desbloqueio ou conexão remota. Se você usar UE-V outras soluções de compartilhamento de configurações, os usuários poderão ter inconsistências em configurações sincronizadas.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>As configurações do aplicativo são específicas do computador? As preferências e personalizações de aplicativos associadas a configurações de hardware ou de computador específicas não são sincronizadas consistentemente entre sessões e podem causar uma experiência de aplicativo ruim.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>As configurações do armazenamento de aplicativos no diretório Arquivos de Programas ou no diretório de arquivos localizado no diretório Usuários [Nome do <strong> </strong> usuário] &lt; forte &gt; AppData </strong> &lt; forte &gt; </strong> LocalLow? Os dados do aplicativo armazenados em qualquer um desses locais geralmente não devem ser sincronizados com o usuário, pois esses dados são específicos do computador ou porque os dados são muito grandes para sincronizar.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>O aplicativo armazena alguma configuração em um arquivo que contém outros dados de aplicativo que não devem ser sincronizados? UE-V sincroniza arquivos como uma única unidade. Se as configurações são armazenadas em arquivos que incluem dados de aplicativos que não sejam configurações, a sincronização de dados adicionais pode causar uma experiência de aplicativo ruim.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Qual é o tamanho dos arquivos que contêm as configurações? O desempenho da sincronização de configurações pode ser afetado por arquivos grandes. Incluir arquivos grandes pode afetar o desempenho da sincronização de configurações.</p></td>
</tr>
</tbody>
</table>



## <a name="other-considerations-when-preparing-a-ue-v-deployment"></a><a href="" id="considerations"></a>Outras considerações ao preparar uma implantação UE-V de dados


Você também deve considerar essas coisas quando estiver se preparando para implantar UE-V:

-   [Gerenciando a sincronização de credenciais](#creds)

-   [Windows sincronização de configurações do aplicativo](#appxsettings)

-   [Modelos UE-V de localização de configurações personalizadas](#custom)

-   [Configurações de configurações de usuário não intencional](#prevent)

-   [Desempenho e capacidade](#capacity)

-   [Alta disponibilidade](#high)

-   [Sincronização do relógio do computador](#clocksync)

### <a name="managing-credentials-synchronization-in-ue-v-21-and-ue-v-21-sp1"></a><a href="" id="creds"></a>Gerenciando a sincronização de credenciais no UE-V 2.1 e UE-V 2.1 SP1

Muitos aplicativos corporativos, incluindo o Microsoft Outlook e o Lync, solicitam aos usuários suas credenciais de domínio no logon. Os usuários têm a opção de salvar suas credenciais no disco para impedir que eles entrem sempre que abrirem esses aplicativos. A habilitação da sincronização de credenciais de roaming permite que os usuários salvem suas credenciais em um computador e evitem inseri-las em todos os computadores que usam em seu ambiente. Os usuários podem sincronizar algumas credenciais de domínio com UE-V 2.1 e 2.1 SP1.

**Importante**  
A sincronização de credenciais está desabilitada por padrão. Você deve habilitar explicitamente a sincronização de credenciais durante a implantação para implementar esse recurso.



UE-V 2.1 e 2.1 SP1 podem sincronizar credenciais corporativas, mas não roam credentials destinados apenas para uso no computador local.

As credenciais são configurações síncronas, o que significa que elas são aplicadas ao seu perfil na primeira vez que você faz logon no computador após UE-V sincronizações.

A sincronização de credenciais é gerenciada por seu próprio modelo de local de configurações, que é desabilitado por padrão. Você pode habilitar ou desabilitar esse modelo por meio dos mesmos métodos usados para outros modelos. O identificador de modelo para esse recurso é RoamingCredentialSettings.

**Importante**  
Se você estiver usando o Roaming de Credenciais do Active Directory em seu ambiente, recomendamos que você não habilita o modelo UE-V de roaming de credenciais.



Use um desses métodos para habilitar a sincronização de credenciais:

-   Centro de Configurações empresa

-   Windows PowerShell

-   Política de Grupo

**Observação**  
As credenciais são criptografadas durante a sincronização.



[Centro Configurações empresa](https://technet.microsoft.com/library/dn458903.aspx)**: marque** a caixa de seleção Credenciais de Roaming Configurações em Windows Configurações para habilitar a sincronização de credenciais. Desmarque a caixa para desabilitá-la. Essa caixa de seleção só será exibida no Centro Configurações empresa se sua conta não estiver configurada para sincronizar configurações usando uma conta da Microsoft.

[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** Este cmdlet do PowerShell habilita a sincronização de credenciais:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Este cmdlet do PowerShell desabilita a sincronização de credenciais:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Política de](https://technet.microsoft.com/library/dn458893.aspx)**Grupo :** você deve implantar o modelo [ADMX MDOP mais](https://go.microsoft.com/fwlink/p/?LinkId=393944) recente para habilitar a sincronização de credenciais por meio da política de grupo. A sincronização de credenciais é gerenciada com as Windows configurações. Para gerenciar esse recurso com a Política de Grupo, habilita a política Sincronizar Windows configurações.

1.  Abra o Editor de Política de Grupo e navegue até Configuração do Usuário **– Modelos Administrativos – Windows Componentes – Microsoft User Experience Virtualization**.

2.  Clique duas vezes em **Sincronizar Windows configurações**.

3.  Se essa política estiver habilitada, você poderá habilitar a sincronização de credenciais verificando a caixa de seleção Credenciais de **Roaming** ou desabilitando a sincronização de credenciais desmarcando-a.

4.  Clique em **OK**.

### <a name="credential-locations-synchronized-by-ue-v"></a>Locais de credenciais sincronizados por UE-V

Os arquivos de credencial salvos pelos aplicativos nos seguintes locais são sincronizados:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

As credenciais salvas em outros locais não são sincronizadas por UE-V.

### <a name="windows-app-settings-synchronization"></a><a href="" id="appxsettings"></a>Windows sincronização de configurações do aplicativo

UE-V gerencia Windows sincronização de configurações do aplicativo de três maneiras:

-   **Sincronizar Windows Aplicativos:** Permitir ou negar qualquer sincronização Windows aplicativos

-   **Windows App List:** Sincronizar uma lista de Windows aplicativos

-   **Comportamento de sincronização padrão não listado:** Determine o comportamento de sincronização Windows aplicativos que não estão na lista Windows aplicativos.

Para obter mais informações, consulte a [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

### <a name="custom-ue-v-settings-location-templates"></a><a href="" id="custom"></a>Modelos UE-V de localização de configurações personalizadas

Se você estiver implantando UE-V para sincronizar configurações para aplicativos personalizados, você usará o gerador UE-V para criar modelos de local de configurações personalizadas para esses aplicativos de área de trabalho. Depois de criar e testar um modelo de local de configurações personalizado em um ambiente de teste, você pode implantar os modelos de local de configurações em computadores da empresa.

Os modelos de local de configurações personalizadas devem ser implantados com uma infraestrutura de implantação existente, como um método de distribuição de software empresarial (ESD), como System Center Configuration Manager, com preferências ou configurando um catálogo de modelos de configurações UE-V. Os modelos implantados com o Configuration Manager ou a Política de Grupo devem ser registrados usando o WMI UE-V ou Windows PowerShell.

Para obter mais informações sobre modelos de local de configurações personalizadas, consulte [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Para obter mais informações sobre como usar UE-V com o Configuration Manager, consulte [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

### <a name="prevent-unintentional-user-settings-configuration"></a><a href="" id="prevent"></a>Impedir configurações não intencional do usuário

UE-V baixa novas informações de configurações do usuário de um local de armazenamento de configurações e aplica as configurações ao computador local nessas instâncias:

-   Sempre que um aplicativo é iniciado que tem um modelo de UE-V registrado.

-   Quando um usuário faz o login em um computador.

-   Quando um usuário desbloqueia um computador.

-   Quando uma conexão é feita com um computador de área de trabalho remota que UE-V instalado.

-   Quando a tarefa agendada do Aplicativo de Controlador de Sincronização é executado.

Se UE-V estiver instalado no computador A e no computador B, e as configurações que você deseja para o aplicativo estão no computador A, então o computador A deve abrir e fechar o aplicativo primeiro. Se o aplicativo for aberto e fechado primeiro no computador B, as configurações do aplicativo no computador A serão configuradas para as configurações do aplicativo no computador B. Configurações são sincronizadas entre computadores por aplicativo. Com o tempo, as configurações se tornam consistentes entre os computadores à medida que são abertas e fechadas com as configurações preferenciais.

Esse cenário também se aplica a Windows configurações. Se as Windows no computador B devem ser as mesmas Windows configurações do computador A, então o usuário deve fazer logoff e fazer logoff do computador A primeiro.

Se as configurações de usuário que o usuário deseja são aplicadas na ordem errada, elas podem ser recuperadas executando uma operação de restauração para o aplicativo específico ou Windows configuração no computador no qual as configurações foram substituídas. Para obter mais informações, consulte [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a name="performance-and-capacity-planning"></a><a href="" id="capacity"></a>Planejamento de desempenho e capacidade

Especifique seus requisitos para UE-V com capacidade de disco padrão e monitoramento de saúde de rede.

UE-V usa um compartilhamento SMB (Server Message Block) para o armazenamento de pacotes de configurações. O tamanho dos pacotes de configurações varia dependendo das informações de configurações de cada aplicativo. Embora a maioria dos pacotes de configurações seja pequena, a sincronização de arquivos potencialmente grandes, como imagens da área de trabalho, pode resultar em um desempenho ruim, especialmente em redes mais lentas.

Para reduzir problemas com latência de rede, crie locais de armazenamento de configurações nas mesmas redes locais onde os computadores dos usuários residem. Recomendamos 20 MB de espaço em disco por usuário para o local de armazenamento de configurações.

Por padrão, UE-V tempo de sincronização após 2 segundos para evitar atraso excessivo devido a um pacote de configurações grandes. Você pode configurar a configuração SyncMethod=SyncProvider usando [Objetos de Política de Grupo](https://technet.microsoft.com/library/dn458893.aspx).

### <a name="high-availability-for-ue-v"></a><a href="" id="high"></a>Alta disponibilidade para UE-V

O UE-V de configurações de armazenamento e o catálogo de modelos de configurações suportam o armazenamento de dados do usuário em qualquer compartilhamento writable. Para garantir alta disponibilidade, siga estes critérios:

-   Formatar o volume de armazenamento com um sistema de arquivos NTFS.

-   O compartilhamento pode usar o DFS (Sistema de Arquivos Distribuídos), mas há restrições.
Especificamente, há suporte para a configuração de destino único do DFS-R (Replicação do Sistema de Arquivos Distribuídos) com ou sem um Namespace do Sistema de Arquivos Distribuídos (DFS-N).
Da mesma forma, somente a configuração de destino único é suportada com DFS-N.
Para obter informações detalhadas, consulte a Instrução de Suporte da [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=313991) sobre dados de perfil de usuário replicados e também Informações sobre a política de suporte da Microsoft para um cenário de implantação [DFS-R e DFS-N.](https://support.microsoft.com/kb/2533009)

    Além disso, como o SYSVOL usa o DFS-R para replicação, o SYSVOL não pode ser usado para UE-V replicação de arquivo de dados.

-   Configure as permissões de compartilhamento e as listas de controle de acesso NTFS (ACLs), conforme especificado em [Deploying the Configurações Armazenamento Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Use o cluster de servidor de arquivos juntamente com o agente UE-V para fornecer acesso a cópias de dados de estado do usuário em caso de falhas de comunicações.

-   Você pode armazenar as configurações dados do caminho de armazenamento (dados do usuário) e modelos de catálogo de modelos de configurações em compartilhamentos agrupados, em compartilhamentos DFS-N ou em ambos.

### <a name="synchronize-computer-clocks-for-ue-v-settings-synchronization"></a><a href="" id="clocksync"></a>Sincronizar relógios de computador para UE-V sincronização de configurações

Os computadores que executarem o UE-V Agent devem usar um servidor de tempo para manter uma experiência de configuração consistente. UE-V usa carimbos de data/hora para determinar se as configurações devem ser sincronizadas a partir do local de armazenamento de configurações. Se o relógio do computador estiver impreciso, as configurações mais antigas podem substituir as configurações mais novas ou as novas configurações podem não ser salvas no local de armazenamento das configurações.

## <a name="confirm-prerequisites-and-supported-configurations-for-ue-v"></a><a href="" id="prereqs"></a>Confirmar pré-requisitos e configurações com suporte para UE-V


Antes de prosseguir, certifique-se de que seu ambiente inclua esses requisitos para executar UE-V.

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
<th align="left"><strong>Service pack</strong></th>
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
<p>.NET Framework 4 ou superior para UE-V 2.0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter ou Web Server</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5 ou superior para UE-V 2,1.</p>
<p>.NET Framework 4 ou superior para UE-V 2.0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 e Windows 8.1</p></td>
<td align="left"><p>Enterprise ou Pro</p></td>
<td align="left"><p>Nenhum</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5 ou superior</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, versão pré-1607</p>
<div class="alert">
<strong>Observação</strong><br/><p>Somente UE-V 2.1 SP1 oferece suporte Windows 10 versão pré-1607</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise ou Pro</p></td>
<td align="left"><p>Nenhum</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 e Windows Server 2012 R2</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>Nenhum</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,5 ou superior</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>Nenhum</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 ou superior</p></td>
<td align="left"><p>.NET Framework 4,6 ou superior</p></td>
</tr>
</tbody>
</table>



Além disso...

-   **Licença MDOP:** Essa tecnologia faz parte do Microsoft Desktop Optimization Pack (MDOP). Enterprise clientes podem obter o MDOP com Microsoft Software Assurance. Para obter mais informações sobre Microsoft Software Assurance e aquisição do MDOP, consulte How Do I Get MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Credenciais Administrativas** para qualquer computador no qual você estará instalando

**Observação**  

-   A partir do WIndows 10, versão 1607, o UE-V está incluído no Windows 10 para [Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e não faz mais parte do Microsoft Desktop Optimization Pack.

-   O UE-V Windows PowerShell do agente UE-V requer .NET Framework 4 ou superior e Windows PowerShell 3,0 ou superior para ser habilitado. Baixe Windows PowerShell 3.0 [aqui](https://go.microsoft.com/fwlink/?LinkId=309609).

-   Instale .NET Framework 4 ou .NET Framework 4.5 em computadores que executem o Windows 7 ou o sistema operacional Windows Server 2008 R2. Os Windows 8, Windows 8.1 e Windows Server 2012 operacionais vêm com .NET Framework 4.5 instalados. O Windows 10 operacional vem com .NET Framework 4.6 instalado.
-   A política "Excluir Cache De Roaming" para perfis obrigatórios não é suportada com UE-V e não deve ser usada.



Não há requisitos especiais de memória de acesso aleatório (RAM) específicos para UE-V.

### <a name="synchronization-of-settings-through-the-sync-provider"></a>Sincronização de Configurações por meio do Provedor de Sincronização

O Provedor de Sincronização é a configuração padrão para os usuários, que sincroniza um cache local com o local de armazenamento de configurações nessas instâncias:

-   Logon/logoff

-   Bloqueio/desbloqueio

-   Conexão/desconexão da área de trabalho remota

-   Aplicativo aberto/fechado

Uma tarefa agendada gerencia essa sincronização de configurações a cada 30 minutos ou por meio de determinados eventos de gatilho para determinados aplicativos. Para obter mais informações, consulte [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

O UE-V Agent sincroniza as configurações do usuário para computadores que nem sempre estão conectados à rede empresarial (computadores remotos e laptops) e computadores que estão sempre conectados à rede (computadores que executem sessões de VDI (interface da área de trabalho virtual) do Windows servidor e host.

**Sincronização para computadores com conexões sempre disponíveis:** Quando você usa o UE-V em computadores que estão sempre conectados à rede, você deve configurar o agente UE-V para sincronizar as configurações usando o parâmetro *SyncMethod=None,* que trata o servidor de armazenamento de configurações como um compartilhamento de rede padrão. Nesta configuração, o agente UE-V pode ser configurado para notificar se a importação das configurações do aplicativo está atrasada.

Habilita essa configuração por meio de um destes métodos:

-   Durante UE-V instalação, no prompt de comando ou em um arquivo em lotes, de definir o parâmetro *AgentSetup.exe SyncMethod = Nenhum*. [A implantação do UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) fornece mais informações.

-   Após UE-V instalação, use o recurso gerenciamento de Configurações no Gerenciador de Configurações do System Center 2012 ou nos modelos ADMX MDOP para pressionar a configuração *SyncMethod = None.*

-   Use Windows PowerShell ou Windows WMI (Instrumentação de Gerenciamento) para definir a configuração *SyncMethod = None.*

    **Observação**  
    Esses dois últimos métodos não funcionam para ambientes de infraestrutura de área de trabalho virtual (VDI) em pool.



Você deve reiniciar o computador antes que as configurações comecem a ser sincronizadas.

**Observação**  
Se você definir *SyncMethod = Nenhum*, quaisquer alterações de configuração serão salvas diretamente no servidor. Se a conexão de rede com o caminho de armazenamento de configurações não for encontrada, as alterações de configurações serão armazenadas em cache no dispositivo e serão sincronizadas na próxima vez em que o provedor de sincronização for executado. Se o caminho de armazenamento de configurações não for encontrado e o perfil de usuário for removido de um ambiente VDI em pool no logoff, as alterações de configurações serão perdidas e o usuário deverá reaplicar a alteração quando o computador for reconectado ao caminho de armazenamento de configurações.



**Sincronização para mecanismos de sincronização externos:** O parâmetro *SyncMethod=External* especifica que, se as configurações do UE-V são escritas em uma pasta local no computador do usuário, qualquer mecanismo de sincronização externo (como OneDrive for Business, Pastas de Trabalho, Sharepoint ou Dropbox) pode ser usado para aplicar essas configurações aos diferentes computadores que os usuários acessam.

**Suporte para sessões VDI compartilhadas:** UE-V 2.1 e 2.1 SP1 oferecem suporte para sessões VDI compartilhadas entre usuários finais. Você pode registrar e configurar um modelo VDI especial, que garante UE-V manter toda a funcionalidade intacta para sessões VDI não persistentes.

**Observação**  
Se você não habilitar o modo VDI para sessões VDI não persistentes, determinados recursos não funcionam, como backup/restauração e último bom [conhecido (LKG)](https://technet.microsoft.com/library/dn878331.aspx).



O modelo VDI é fornecido com UE-V 2.1 e 2.1 SP1 e normalmente está disponível aqui após a instalação: C:\\Arquivos de Programas\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml

### <a name="prerequisites-for-ue-v-generator-support"></a>Pré-requisitos para suporte UE-V Gerador

Instale o UE-V gerador no computador usado para criar modelos de local de configurações personalizadas. Esse computador deve ser capaz de executar os aplicativos cujas configurações estão sincronizadas. Você deve ser membro do grupo Administradores no computador que executa o software UE-V Generator.

O UE-V Generator deve ser instalado em um computador que usa um sistema de arquivos NTFS. O UE-V de gerador requer .NET Framework 4. Para obter mais informações, [consulte Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## <a name="other-resources-for-this-product"></a>Outros recursos para este produto


-   [Microsoft User Experience Virtualization (UE-V) 2.x](index.md)

-   [Introdução ao UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Administrando UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Solução de UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














