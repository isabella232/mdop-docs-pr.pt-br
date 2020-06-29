---
title: Configurando o UE-V 2. x com objetos de política de grupo
description: Configurando o UE-V 2. x com objetos de política de grupo
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799469"
---
# Configurando o UE-V 2. x com objetos de política de grupo


Algumas configurações da política de grupo do Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 podem ser definidas para computadores e outras configurações de política de grupo podem ser definidas para os usuários. Para obter informações sobre como instalar os arquivos ADMX da política de grupo do UE-V, consulte [instalando os modelos ADMX da política de grupo UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).

As configurações de política a seguir podem ser configuradas para UE-V.

**Configurações da Política de Grupo**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da configuração da política de grupo</th>
<th align="left">Target</th>
<th align="left">Descrição da configuração da política de grupo</th>
<th align="left">Opções de configuração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Texto do link de ti de contato</p></td>
<td align="left"><p>Computadores apenas</p></td>
<td align="left"><p>Essa configuração de política de grupo especifica o texto do hiperlink de URL do contato no centro de configurações da empresa.</p></td>
<td align="left"><p>Se você habilitar essa configuração de política de grupo, o centro de configurações da empresa exibirá o texto especificado no link para a URL do contato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL de contato</p></td>
<td align="left"><p>Computadores apenas</p></td>
<td align="left"><p>Essa configuração de política de grupo especifica a URL do link para o contato no centro de configurações da empresa.</p></td>
<td align="left"><p>Se você habilitar essa configuração, o texto de contato do centro de configurações da empresa entrará em contato com a URL especificada. O link pode ser de qualquer protocolo padrão, como HTTP ou mailto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Não usar o provedor de sincronização</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Usando essa configuração de política de grupo, você pode configurar se o UE-V usa o recurso do provedor de sincronização. Essa configuração de política também permite que você habilite a notificação para que ela seja exibida quando a importação das configurações do usuário for adiada.</p></td>
<td align="left"><p>Habilite essa configuração para configurar o UE-V Agent para não usar o provedor de sincronização.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Notificação de primeira utilização</p></td>
<td align="left"><p>Computadores apenas</p></td>
<td align="left"><p>Essa configuração de política de grupo permite uma notificação na área de notificação que aparece quando a UE-V</p>
<p>o agente é executado pela primeira vez.</p></td>
<td align="left"><p>O padrão é habilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações de roaming do Windows</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política de grupo define a sincronização das configurações do Windows.</p></td>
<td align="left"><p>Selecione as configurações do Windows que são sincronizadas entre computadores.</p>
<p>Por padrão, os temas do Windows, as configurações da área de trabalho e as configurações de facilidade de acesso sincronizam as configurações entre computadores da mesma versão do sistema operacional.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Limite de aviso de tamanho do pacote de configurações</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política de grupo permite que você configure o UE-V Agent para denunciar quando um tamanho de arquivo de pacote de configurações atingir um limite definido.</p></td>
<td align="left"><p>Especifique o limite preferencial para o tamanho do pacote de configurações em kilobytes (KB).</p>
<p>Por padrão, o UE-V Agent não tem um limite de tamanho de arquivo de pacote.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Caminho de armazenamento de configurações</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política de grupo define onde as configurações do usuário devem ser armazenadas.</p></td>
<td align="left"><p>Digite um caminho UNC (Convenção Universal de nomenclatura) e variáveis como \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Caminho do catálogo de modelos de configurações</p></td>
<td align="left"><p>Computadores apenas</p></td>
<td align="left"><p>Essa configuração de política de grupo define onde os modelos de localização de configurações personalizadas são armazenados. Essa configuração de política também define se o catálogo deve ser usado para substituir os modelos padrão da Microsoft que são instalados com o UE-V Agent.</p></td>
<td align="left"><p>Insira um caminho UNC (Convenção Universal de nomenclatura) como \Server\TemplateShare ou um local de pasta no computador.</p>
<p>Marque a caixa de seleção para substituir os modelos padrão da Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar configurações em conexões limitadas</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política de grupo define se o UE-V sincroniza as configurações em conexões limitadas.</p></td>
<td align="left"><p>Por padrão, o UE-V Agent não sincroniza as configurações em uma conexão limitada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizar configurações em conexões limitadas, mesmo durante o roaming</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política de grupo define se o UE-V sincronizará as configurações em conexões limitadas fora da rede do provedor primário, por exemplo, quando a conexão de dados estiver em modo de roaming.</p></td>
<td align="left"><p>Por padrão, o UE-V não sincroniza as configurações em uma conexão limitada quando está em modo de roaming.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tempo limite de sincronização</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política de grupo configura o número de milissegundos que o computador aguarda antes de um tempo limite quando ele recupera as configurações de usuário do local de configurações remotas. Se o local do armazenamento remoto não estiver disponível e o usuário não usar o provedor de sincronização, o início do aplicativo será atrasado por esse número de milissegundos.</p></td>
<td align="left"><p>Especifique o tempo limite de sincronização preferencial em milissegundos. O valor padrão é 2000 milissegundos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ícone de bandeja</p></td>
<td align="left"><p>Computadores apenas</p></td>
<td align="left"><p>Essa configuração de política de grupo habilita o ícone de bandeja do User Experience Virtualization (UE-V).</p></td>
<td align="left"><p>O padrão é habilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usar a User Experience Virtualization (UE-V)</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política de grupo permite habilitar ou desabilitar a virtualização da experiência do usuário (UE-V).</p></td>
<td align="left"><p>Habilitar ou desabilitar essa configuração de política de grupo.</p></td>
</tr>
</tbody>
</table>

 

**Observação**  Além disso, as configurações de política de grupo estão disponíveis para muitos aplicativos da área de trabalho e aplicativos do Windows. Você pode usar essas configurações para habilitar ou desabilitar a sincronização de configurações para aplicativos específicos.

 

**Configurações da política de grupo do aplicativo Windows**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da configuração da política de grupo</th>
<th align="left">Target</th>
<th align="left">Descrição da configuração da política de grupo</th>
<th align="left">Opções de configuração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Não sincronizar aplicativos do Windows</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política de grupo define se o UE-V Agent sincroniza as configurações para aplicativos do Windows.</p></td>
<td align="left"><p>O padrão é sincronizar aplicativos do Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Lista de aplicativos do Windows</p></td>
<td align="left"><p>Computador e usuário</p></td>
<td align="left"><p>Esta configuração lista os nomes dos pacotes familiares dos aplicativos e Estados do Windows expressamente se a UE-V sincroniza as configurações do aplicativo.</p></td>
<td align="left"><p>Você pode usar essa configuração para especificar que as configurações de um aplicativo nunca sejam sincronizadas pelo UE-V, mesmo se as configurações de todos os outros aplicativos do Windows estiverem sincronizadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar aplicativos do Windows não listados</p></td>
<td align="left"><p>Computador e usuário</p></td>
<td align="left"><p>Essa configuração de política de grupo define o comportamento de sincronização de configurações padrão do UE-V Agent para aplicativos do Windows que não estão explicitamente listados na lista de aplicativos do Windows.</p></td>
<td align="left"><p>Por padrão, o UE-V Agent sincroniza apenas as configurações dos aplicativos do Windows que estão incluídos na lista de aplicativos do Windows.</p></td>
</tr>
</tbody>
</table>

 

Para obter mais informações sobre a sincronização de aplicativos do Windows, consulte [lista de aplicativos do Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

**Para definir configurações de política de grupo direcionadas a computador**

1.  Use o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) no computador que atua como um controlador de domínio para gerenciar as configurações de política de grupo para computadores UE-V. Navegue até **configuração do computador**, **selecione políticas**, selecione **modelos administrativos**, clique em **componentes do Windows**e selecione **virtualização da experiência do usuário da Microsoft**.

2.  Selecione a configuração de política de grupo a ser editada.

**Para definir configurações de política de grupo direcionadas ao usuário**

1.  Use o GPMC (console de gerenciamento de política de grupo) ou a ferramenta de gerenciamento avançado de política de grupo (AGPM) no Microsoft Desktop Optimization Pack (MDOP) no computador do controlador de domínio para gerenciar as configurações de política de grupo para UE-V. Navegue até **configuração do usuário**, **selecione políticas**, selecione **modelos administrativos**, clique em **componentes do Windows**e selecione **virtualização da experiência do usuário da Microsoft**.

2.  Selecione a configuração de política de grupo editada.

O UE-V Agent usa a seguinte ordem de precedência para determinar a sincronização.

**Ordem de precedência para configurações de UE-V**

1.  Configurações direcionadas ao usuário que são gerenciadas por configurações de política de grupo-essas configurações são armazenadas na chave do registro por política de grupo em `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Configurações direcionadas por computador que são gerenciadas por configurações de política de grupo-essas configurações são armazenadas na chave do registro por política de grupo em `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  As definições de configuração que são definidas pelo usuário atual usando o Windows PowerShell ou WMI (Instrumentação de gerenciamento do Windows)-essas configurações são armazenadas pelo UE-V Agent sob este local de registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Configurações definidas para o computador usando o Windows PowerShell ou o WMI. Essas configurações são armazenadas pelo UE-V Agent sob este local de registro: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .

    **Tem uma sugestão para UE-V**? Adicione ou vote em sugestões [aqui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Tem um problema de UE-V**? Use o [Fórum do TechNet para UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Tópicos relacionados


[Administração do UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Gerenciar as configurações da UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





