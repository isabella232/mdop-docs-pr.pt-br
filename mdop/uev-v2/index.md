---
title: Microsoft User Experience Virtualization (UE-V) 2.x
description: Microsoft User Experience Virtualization (UE-V) 2.x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 79748e04ae1a59afdc8f9dae3c5dc77c50e3c253
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910536"
---
# <a name="microsoft-user-experience-virtualization-ue-v-2x"></a>Microsoft User Experience Virtualization (UE-V) 2.x

>[!NOTE]
>Esta documentação é uma versão para UE-V que foi incluída no Microsoft Desktop Optimization Pack (MDOP). Para obter informações sobre a versão mais recente do UE-V que está incluída no Windows 10 Enterprise, consulte [Introdução com UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Capture e centralize as configurações de aplicativos e Windows do sistema operacional dos usuários implementando o Microsoft User Experience Virtualization (UE-V) 2.0 ou 2.1. Em seguida, aplique essas configurações aos dispositivos que os usuários acessam em sua empresa, como computadores desktop, laptops ou sessões de VDI (infraestrutura de área de trabalho virtual).

**Com UE-V você pode...**

-   Especificar quais configurações de aplicativo e área de trabalho sincronizam

-   Oferecer as configurações a qualquer momento e em qualquer lugar onde os usuários trabalhem em toda a empresa

-   Criar modelos personalizados para os aplicativos de terceiros ou de linha de negócios

-   Recuperar configurações após a substituição ou atualização de hardware ou depois de recuperar uma máquina virtual para seu estado inicial

## <a name="components-of-ue-v-2x"></a>Componentes do UE-V 2.x


Este diagrama mostra como os componentes UE-V implantados trabalham juntos para sincronizar as configurações.

![Diagrama de arquitetura uev2.](images/uev2archdiagram.gif)

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
<td align="left"><p><strong>UE-V Agente</strong></p></td>
<td align="left"><p>Instalado em todos os computadores que precisam sincronizar configurações, o agente UE-V monitora aplicativos registrados e o sistema operacional para quaisquer alterações de configurações e, em seguida, sincroniza essas configurações entre <strong> </strong> computadores.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Configurações pacotes</strong></p></td>
<td align="left"><p>As configurações de aplicativo e Windows são armazenadas em pacotes <strong> de configurações </strong> criados pelo UE-V Agent. Os pacotes de configurações são criados, armazenados localmente e copiados para o local de armazenamento das configurações.</p>
<ul>
<li><p>Os valores de configuração para aplicativos da área de trabalho <strong> </strong> são armazenados quando o usuário fecha o aplicativo.</p></li>
<li><p>Os valores Windows configurações são armazenados quando o usuário faz o login, quando o computador está bloqueado ou quando o usuário se <strong> </strong> desconecta remotamente de um computador.</p></li>
</ul>
<p>O provedor de sincronização determina quando as configurações do aplicativo ou do sistema operacional são lidas Configurações <strong> Pacotes </strong> e sincronizadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Configurações local de armazenamento</strong></p></td>
<td align="left"><p>Esse é um compartilhamento de rede padrão que seus usuários podem acessar. O UE-V Agente verifica o local e cria uma pasta oculta do sistema na qual armazenar e recuperar as configurações do usuário.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Configurações de localização</strong></p></td>
<td align="left"><p>UE-V usa arquivos XML como modelos de localização de configurações para monitorar e sincronizar configurações de aplicativos de área de trabalho e Windows de área de trabalho entre computadores de usuário. Por padrão, alguns modelos de local de configurações são incluídos em UE-V . Você também pode criar, editar ou validar modelos de local de configurações personalizadas gerenciando a sincronização de configurações <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> para aplicativos personalizados. </a></p>
<div class="alert">
<strong>Observação</strong><br/><p>Configurações de local não são necessários para Windows aplicativos.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows de aplicativos</strong></p></td>
<td align="left"><p>Configurações para Windows aplicativos são capturados e aplicados dinamicamente. O desenvolvedor do aplicativo especifica as configurações sincronizadas para cada aplicativo. UE-V determina quais aplicativos Windows estão habilitados para sincronização de configurações usando uma lista gerenciada de aplicativos. Por padrão, essa lista inclui a maioria dos Windows aplicativos.</p>
<p>Você pode adicionar ou remover aplicativos na lista de aplicativos Windows seguindo os procedimentos <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> mostrados aqui </a> .</p></td>
</tr>
</tbody>
</table>



### <a name="managing-settings-synchronization-for-custom-applications"></a><a href="" id="customapps"></a>Gerenciando Configurações sincronização para aplicativos personalizados

Use esses UE-V para criar e gerenciar modelos personalizados para seus aplicativos de terceiros ou de linha de negócios.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V Gerador</strong></p></td>
<td align="left"><p>Use o UE-V Gerador para criar modelos de local de configurações personalizadas que você pode distribuir para <strong> </strong> computadores do usuário. O UE-V Generator também permite editar um modelo existente ou validar um modelo criado usando outro editor XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Configurações catálogo de modelos</strong></p></td>
<td align="left"><p>O catálogo de modelos de configurações é um caminho de pasta em computadores UE-V ou um compartilhamento de rede <strong> do SMB (Server Message Block) que armazena os modelos de local de configurações </strong> personalizadas. O UE-V agente verifica esse local uma vez por dia, recupera modelos novos ou atualizados e atualiza seu comportamento de sincronização.</p>
<p>Se você usar apenas os UE-V de local de configurações padrão, um catálogo de modelos de configurações será desnecessário. Para obter mais informações sobre configurações de catálogos de implantação, consulte <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> Configure a UE-V settings template catalog </a> .</p></td>
</tr>
</tbody>
</table>



![Processo do gerador ue-v.](images/ue-vgeneratorprocess.gif)

## <a name="settings-synchronized-by-default"></a>Configurações Sincronizado por padrão


UE-V sincroniza configurações para esses aplicativos por padrão. Para obter uma lista completa e informações mais detalhadas, consulte Configurações que são sincronizadas automaticamente [em uma UE-V implantação](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).

Microsoft Office aplicativos 2013 (UE-V 2.1 SP1 e 2.1)

Microsoft Office aplicativos 2010 (UE-V 2.1 SP1, 2.1 e 2.0)

Microsoft Office aplicativos 2007 (UE-V somente 2.0)

Internet Explorer 8, 9 e 10

Internet Explorer 11 em UE-V 2.1 SP1 e 2.1

Muitos Windows aplicativos, como o Xbox

Muitos Windows de área de trabalho, como Bloco de notas

Muitas Windows, como plano de fundo da área de trabalho ou papel de parede

**Observação**  
Você também pode [personalizar UE-V para sincronizar](https://technet.microsoft.com/library/dn458942.aspx) configurações para aplicativos diferentes daqueles sincronizados por padrão.



## <a name="compare-ue-v-to-other-microsoft-products"></a>Comparar UE-V com outros produtos Microsoft


Use esta tabela para comparar UE-V a Sincronizar Perfis no Windows 7, Sincronizar Perfis no Windows 8 e o recurso Sincronizar Configurações pc da conta da Microsoft.

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
<th align="left">Sincronizar perfis usando Windows 7</th>
<th align="left">Sincronizar perfis usando Windows 8</th>
<th align="left">Sincronizar perfis usando Windows 10</th>
<th align="left">Conta Microsoft</th>
<th align="left">UE-V 2.0</th>
<th align="left">UE-V 2.1 e 2.1 SP1</th>
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
<td align="left"><p>Sincronizar Windows configurações do aplicativo</p></td>
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
<td align="left"><p>Sincronizar as alterações de configurações regularmente</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuração mínima para Instalação</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Suportado em computadores não ingressados no domínio</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Dá suporte ao atributo Primary Computer Active Directory</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincroniza as configurações entre a infraestrutura de área de trabalho virtual (VDI)/Serviços de Área de Trabalho Remota (RDS) e áreas de trabalho ricas</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espaço de armazenamento de configuração ilimitado</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Escolha em que configurações de aplicativo sincronizar</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Backup/restauração para Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Parcial</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## <a name="ue-v-2x-release-notes"></a>UE-V Notas de versão 2.x


Para obter mais informações e notícias de última hora que não entraram na documentação, consulte

-   [Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 SP1 da Microsoft](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.1 da Microsoft](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Notas de versão da Virtualização de Experiência do Usuário (UE-V) 2.0 da Microsoft](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <a name="other-resources-for-this-product"></a>Outros recursos para este produto


-   [Introdução ao UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Preparar uma implantação UE-V 2.x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Administrando UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Solução de UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Referência técnica da UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### <a name="more-information"></a>Mais informações

<a href="" id="mdop-techcenter-page"></a>[Página do TechCenter do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Saiba mais sobre as informações e recursos mais recentes do MDOP.

<a href="" id="mdop-information-experience"></a>[Experiência de Informações do MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Encontre documentação, vídeos e outros recursos para tecnologias MDOP. Você também pode [nos enviar comentários ou](mailto:MDOPDocs@microsoft.com) saber mais sobre atualizações nos seguindo no [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter.](https://go.microsoft.com/fwlink/p/?LinkId=242447)














