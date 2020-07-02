---
title: Microsoft User Experience Virtualization (UE-V) 2. x
description: Microsoft User Experience Virtualization (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795442"
---
# Microsoft User Experience Virtualization (UE-V) 2. x

>[!NOTE]
>Esta documentação é uma versão do para o UE-V incluída no Microsoft Desktop Optimization Pack (MDOP). Para obter informações sobre a versão mais recente do UE-V que está incluída no Windows 10 Enterprise, consulte [introdução ao UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Capture e centralize as configurações do aplicativo do usuário e as configurações do sistema operacional do Windows implementando o Microsoft User Experience Virtualization (UE-V) 2,0 ou 2,1. Em seguida, aplique essas configurações aos dispositivos que os usuários acessam na sua empresa, como computadores de mesa, laptops ou sessões do Virtual Desktop Infrastructure (VDI).

**Com a UE-V, você pode...**

-   Especificar quais configurações de aplicativo e área de trabalho sincronizar

-   Oferecer as configurações a qualquer momento e em qualquer lugar onde os usuários trabalhem em toda a empresa

-   Criar modelos personalizados para os aplicativos de terceiros ou de linha de negócios

-   Recuperar as configurações após a substituição ou atualização de hardware ou depois de refazer a criação de uma nova imagem de uma máquina virtual para seu estado inicial

## Componentes da UE-V 2. x


Este diagrama mostra como implantados componentes do UE-V trabalham em conjunto para sincronizar as configurações.

![diagrama arquitetônico uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">Função</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V Agent</strong></p></td>
<td align="left"><p>Instalado em cada computador que precisa sincronizar as configurações, o <strong> UE-V Agent </strong> monitora os aplicativos registrados e o sistema operacional em busca de alterações de configurações e, em seguida, sincroniza essas configurações entre computadores.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Pacotes de configurações</strong></p></td>
<td align="left"><p>As configurações do aplicativo e as configurações do Windows são armazenadas em <strong> pacotes de configurações </strong> criados pelo UE-V Agent. Os pacotes de configurações são criados, armazenados localmente e copiados para o local de armazenamento das configurações.</p>
<ul>
<li><p>Os valores de configuração para <strong> aplicativos da área de trabalho </strong> são armazenados quando o usuário fecha o aplicativo.</p></li>
<li><p>Os valores das <strong> configurações do Windows </strong> são armazenados quando o usuário faz logoff, quando o computador está bloqueado ou quando o usuário se desconecta remotamente de um computador.</p></li>
</ul>
<p>O provedor de sincronização determina quando as configurações do aplicativo ou do sistema operacional são lidas a partir dos <strong> pacotes de configurações </strong> e sincronizadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Local de armazenamento de configurações</strong></p></td>
<td align="left"><p>Esse é um compartilhamento de rede padrão que os usuários podem acessar. O UE-V Agent verifica o local e cria uma pasta de sistema oculta para armazenar e recuperar as configurações do usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Modelos de local de configurações</strong></p></td>
<td align="left"><p>O UE-V usa os arquivos XML como modelos de localização de configurações para monitorar e sincronizar as configurações de aplicativo da área de trabalho e as configurações da área de trabalho do Windows entre computadores Por padrão, alguns modelos de local de configurações estão incluídos na UE-V. Você também pode criar, editar ou validar modelos de local de configurações personalizadas ao <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> gerenciar a sincronização de configurações para aplicativos personalizados </a> .</p>
<div class="alert">
<strong>Observação</strong><br/><p>Os modelos de local de configurações não são necessários para aplicativos do Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Lista de aplicativos do Windows</strong></p></td>
<td align="left"><p>As configurações para aplicativos do Windows são capturadas e aplicadas dinamicamente. O desenvolvedor do aplicativo especifica as configurações que são sincronizadas para cada aplicativo. O UE-V determina quais aplicativos do Windows estão habilitados para sincronização de configurações usando uma lista gerenciada de aplicativos. Por padrão, essa lista inclui a maioria dos aplicativos do Windows.</p>
<p>Você pode adicionar ou remover aplicativos na lista de aplicativos do Windows seguindo os procedimentos mostrados <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> aqui </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a>Gerenciando a sincronização de configurações para aplicativos personalizados

Use estes componentes UE-V para criar e gerenciar modelos personalizados para seus aplicativos de terceiros ou de linha de negócios.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Gerador de UE-V</strong></p></td>
<td align="left"><p>Use o <strong> UE-V Generator </strong> para criar modelos de localização de configurações personalizadas que você pode distribuir para os computadores dos usuários. O gerador UE-V também permite que você edite um modelo existente ou valide um modelo que foi criado usando outro editor de XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Catálogo de modelos de configurações</strong></p></td>
<td align="left"><p>O <strong> Catálogo de modelos de configurações </strong> é um caminho de pasta em computadores UE-V ou um compartilhamento de rede de servidor de mensagens de servidor (SMB) que armazena os modelos de local de configurações personalizadas. O UE-V Agent verifica esse local uma vez por dia, recupera modelos novos ou atualizados e atualiza seu comportamento de sincronização.</p>
<p>Se você usar somente os modelos de local de configurações padrão do UE-V, um catálogo de modelos de configurações será desnecessário. Para obter mais informações sobre os catálogos de implantação de configurações, consulte <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> configurar um catálogo de modelos de configurações de UE-V </a> .</p></td>
</tr>
</tbody>
</table>



![processo de gerador de UE-v](images/ue-vgeneratorprocess.gif)

## Configurações sincronizadas por padrão


Por padrão, o UE-V sincroniza as configurações desses aplicativos. Para obter uma lista completa e informações mais detalhadas, consulte [configurações que são sincronizadas automaticamente em uma implantação do UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).

Aplicativos do Microsoft Office 2013 (UE-V 2,1 SP1 e 2,1)

Aplicativos do Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 e 2,0)

Aplicativos do Microsoft Office 2007 (somente para o UE-V 2,0)

Internet Explorer 8, 9 e 10

Internet Explorer 11 no UE-V 2,1 SP1 e 2,1

Muitos aplicativos do Windows, como o Xbox

Muitos aplicativos da área de trabalho do Windows, como o bloco de notas

Muitas configurações do Windows, como plano de fundo da área de trabalho ou papel de parede

**Observação**  
Você também pode [Personalizar o UE-V para sincronizar as configurações](https://technet.microsoft.com/library/dn458942.aspx) de aplicativos diferentes das sincronizadas por padrão.



## Comparar o UE-V com outros produtos da Microsoft


Use esta tabela para comparar o UE-V para sincronizar perfis no Windows 7, sincronizar perfis no Windows 8 e o recurso configurações do computador de sincronização da conta da Microsoft.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Recurso</th>
<th align="left">Sincronizar perfis usando o Windows 7</th>
<th align="left">Sincronizar perfis usando o Windows 8</th>
<th align="left">Sincronizar perfis usando o Windows 10</th>
<th align="left">Conta Microsoft</th>
<th align="left">UE-V 2,0</th>
<th align="left">UE-V 2,1 e 2,1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sincronizar configurações entre vários computadores</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizar configurações entre aplicativos físicos e virtuais</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar configurações do aplicativo do Windows</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gerenciar via WMI</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar alterações de configurações regularmente</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuração mínima para a instalação</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Com suporte em computadores não associados ao domínio</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Compatível com o atributo do Active Directory do computador principal</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincroniza as configurações entre os serviços de área de trabalho (RDS) e os serviços de área de trabalho avançados do Virtual Desktop Infrastructure (VDI)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espaço de armazenamento de configuração ilimitada</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolha de quais configurações do aplicativo sincronizar</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Backup/restauração para profissionais de ti</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Parcial</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## Notas da versão do UE-V 2. x


Para saber mais e saber mais sobre as últimas notícias que não o fizeram na documentação, consulte

-   [Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 SP1 da Microsoft](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 da Microsoft](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## Outros recursos para este produto


-   [Introdução ao UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Preparar uma implantação do UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Solução de problemas do UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### Mais informações

<a href="" id="mdop-techcenter-page"></a>[Página do TechCenter do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Saiba mais sobre as informações e os recursos mais recentes do MDOP.

<a href="" id="mdop-information-experience"></a>[Experiência de informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Encontre documentação, vídeos e outros recursos para tecnologias do MDOP. Você também pode [enviar comentários](mailto:MDOPDocs@microsoft.com) ou saber mais sobre atualizações seguindo-nos no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).














