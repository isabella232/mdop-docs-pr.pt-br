---
title: Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0
description: Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795994"
---
# Planejar quais aplicativos devem ser sincronizados com a UE-V 1.0


O Microsoft User Experience Virtualization (UE-V) usa modelos de local de configurações (arquivos XML) que definem as configurações que são capturadas e aplicadas pela UE-V. O UE-V inclui um conjunto de modelos de locais de configurações predefinidos e também permite que os administradores criem modelos de localização de configurações personalizadas para aplicativos de terceiros ou de linha de negócios que são usados na empresa.

Como administrador, quando você considera quais aplicativos incluir em sua solução UE-V, considere quais configurações podem ser personalizadas pelos usuários e como e onde o aplicativo armazena suas configurações. Nem todos os aplicativos têm configurações que podem ser personalizadas ou que são rotineiramente personalizadas pelos usuários. Além disso, nem todas as configurações de aplicativos podem fazer roaming segura entre vários computadores ou ambientes. Sincronize as configurações que atendem aos seguintes critérios:

-   Configurações armazenadas em locais acessíveis pelo usuário. Por exemplo, não sincronize as configurações que são armazenadas na seção HKCU ou externa HKCU do registro.

-   Configurações que não são específicas do computador específico. Por exemplo, exclua configurações de rede ou de hardware.

-   Configurações que podem ser sincronizadas entre computadores sem risco de dados corrompidos. Por exemplo, não use configurações armazenadas em um arquivo de banco de dados.

## Modelos de local de configurações incluídos na UE-V


**Modelos de local das configurações do aplicativo UE-V**

O software de instalação do UE-V Agent instala o agente e registra um grupo padrão de modelos de local de configurações para aplicativos comuns da Microsoft. Esses modelos de local de configurações capturam valores de configurações para os seguintes aplicativos:

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
<td align="left"><p>Aplicativos do Microsoft Office 2010</p></td>
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
<p>Microsoft OneNote 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Opções do navegador (Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10)</p></td>
<td align="left"><p>Favoritos, página inicial, guias e barras de ferramentas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Acessórios do Windows</p></td>
<td align="left"><p>Calculadora, bloco de notas, bloco de notas.</p></td>
</tr>
</tbody>
</table>

 

As configurações do aplicativo são aplicadas ao aplicativo quando o aplicativo é iniciado. Eles são salvos quando o aplicativo é fechado.

**Modelos de localização de configurações do Windows para UE-V**

A virtualização da experiência do usuário inclui modelos de local de configurações que capturam valores de configurações para as seguintes configurações do Windows:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">configurações do Windows</th>
<th align="left">Descrição</th>
<th align="left">Aplicar em</th>
<th align="left">Estado padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tela de fundo da área de trabalho</p></td>
<td align="left"><p>Plano de fundo da área de trabalho ativa no momento.</p></td>
<td align="left"><p>Logon, desbloquear, conexão remota.</p></td>
<td align="left"><p>Habilitado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Facilidade de Acesso</p></td>
<td align="left"><p>As configurações de acessibilidade e de entrada, a lupa, o narrador e o teclado virtual.</p></td>
<td align="left"><p>Logon, desbloquear, conexão remota.</p></td>
<td align="left"><p>Desabilitado</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações da área de trabalho</p></td>
<td align="left"><p>Menu iniciar e configurações da barra de tarefas, opções de pasta, ícones da área de trabalho padrão, relógios adicionais e configurações de região e idioma.</p></td>
<td align="left"><p>Somente logon.</p></td>
<td align="left"><p>Desabilitado</p></td>
</tr>
</tbody>
</table>

 

As configurações de plano de fundo da área de trabalho do Windows e facilidade de acesso são aplicadas quando o usuário faz logon, quando o computador é desbloqueado ou na conexão remota com outro computador. O agente salva essas configurações quando o usuário faz logoff, quando o computador está bloqueado ou quando uma conexão remota é desconectada. Por padrão, as configurações de plano de fundo da área de trabalho do Windows são feitas em roaming entre computadores da mesma versão do sistema operacional.

As configurações de facilidade de acesso e área de trabalho do Windows são aplicadas ao fazer logon antes que a área de trabalho seja apresentada ao usuário. Para otimizar a experiência de logon, essas configurações não são em roaming por padrão. As configurações de área de trabalho e facilidade de acesso podem ser habilitadas usando a política de grupo, o PowerShell e o WMI.

O UE-V não é compatível com o roaming de configurações entre sistemas operacionais com idiomas diferentes. Por exemplo, não há suporte para a sincronização entre inglês e alemão. O idioma de todos os computadores para os quais o UE-V transfere as configurações do usuário devem coincidir.

**Observação**  Se você alterar os modelos de local de configurações fornecidos pela Microsoft, o User Experience Virtualization poderá não funcionar corretamente para o aplicativo designado ou o grupo de configurações do Windows.

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a>Impedir a configuração de configurações do usuário não intencional


A virtualização da experiência do usuário verifica se há novas informações nas configurações do usuário e baixa essas informações de acordo com um local de armazenamento de configurações. Em seguida, ele aplica as configurações ao computador local nos seguintes casos:

-   Toda vez que um aplicativo é iniciado com um modelo UE-V registrado.

-   Quando um usuário faz logon no computador dele.

-   Quando um usuário desbloqueia o computador.

-   Quando é feita uma conexão com um computador de área de trabalho remota com UE-V instalado.

Se o UE-V estiver instalado no computador A e no computador B, e as configurações desejadas para o aplicativo estiverem no computador A, o computador A deve abrir e fechar o aplicativo primeiro. Se um aplicativo for aberto e fechado no computador B primeiro, as configurações do aplicativo no computador A serão configuradas para serem iguais às configurações do aplicativo no computador B.

Esse cenário também se aplica às configurações do Windows. Se as configurações do Windows no computador B devem ser iguais às do Windows no computador A, o usuário deve fazer logon e logoff do computador primeiro.

Se as configurações de usuário desejadas forem aplicadas na ordem errada, poderão ser recuperadas ao executar uma operação de restauração para o aplicativo específico ou a configuração do Windows no computador em que as configurações foram sobrescritas. Para obter mais informações, consulte [restaurando as configurações do aplicativo e do Windows sincronizadas com o UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).

## Modelos de localização de configurações personalizadas de UE-V


Você pode criar modelos de local de configurações personalizadas usando o UE-V Generator. Depois de criar e testar um modelo de local de configurações personalizado em um ambiente de teste, você pode implantar os modelos de local de configurações em computadores na empresa. Modelos de localização de configurações personalizadas devem ser implantados com uma infraestrutura de implantação existente, como o método ESD (Enterprise Software Distribution), com preferências ou configuração de um catálogo de modelos de configurações do UE-V. Os modelos implantados com ESD ou política de grupo devem ser registrados usando o UE-V WMI ou o PowerShell. Para obter mais informações sobre modelos de localização de configurações personalizadas, consulte [planejando a implantação de modelos personalizados para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

Para obter orientação sobre se um aplicativo de linha de negócios deve ser sincronizado, consulte a [lista de verificação para avaliar aplicativos de linha de negócios para o UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).

## Tópicos relacionados


[Planejamento para a UE-V 1.0](planning-for-ue-v-10.md)

[Planejar a implantação de modelo personalizado para a UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Implantação da UE-V 1.0](deploying-ue-v-10.md)

 

 





