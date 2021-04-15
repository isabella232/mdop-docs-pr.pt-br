---
title: Configurando o UE-V 2.x com objetos de política de grupo
description: Configurando o UE-V 2.x com objetos de política de grupo
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
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494056"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a>Configurando o UE-V 2.x com objetos de política de grupo


Algumas configurações da Política de Grupo da Experiência do Usuário da Microsoft (UE-V) 2.0, 2.1 e 2.1 SP1 podem ser definidas para computadores, e outras configurações de Política de Grupo podem ser definidas para os usuários. Para obter informações sobre como instalar arquivos ADMX da Política de Grupo UE-V, consulte [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).

As configurações de política a seguir podem ser configuradas para o UE-V.

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
<th align="left">Nome da configuração da Política de Grupo</th>
<th align="left">Target</th>
<th align="left">Descrição da configuração da Política de Grupo</th>
<th align="left">Opções de configuração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurar o método Sync</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Usando essa configuração de Política de Grupo, você pode configurar se a UE-V (User Experience Virtualization) usa o recurso do provedor de sincronização. Essa configuração de política também permite que uma notificação apareça quando a importação de configurações do usuário é adiada.</p></td>
<td align="left"><p>Habilita essa configuração para configurar o agente UE-V para não usar o provedor de sincronização ou para usar o mecanismo de sincronização externo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Entrar em contato com o texto do link de IT</p></td>
<td align="left"><p>Somente computadores</p></td>
<td align="left"><p>Esta configuração de Política de Grupo especifica o texto do hiperlink da URL de Contato na Central de Configurações da Empresa.</p></td>
<td align="left"><p>Se você habilitar essa configuração de Política de Grupo, o Centro de Configurações da Empresa exibirá o texto especificado no link para a URL de TI de contato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Entrar em contato com a URL de IT</p></td>
<td align="left"><p>Somente computadores</p></td>
<td align="left"><p>Esta configuração de Política de Grupo especifica a URL do link Contato de IT na Central de Configurações da Empresa.</p></td>
<td align="left"><p>Se você habilitar essa configuração, o Centro de Configurações da Empresa contatará links de texto de TI para a URL especificada. O link pode ser de qualquer protocolo padrão, como HTTP ou mailto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Notificação de Primeiro Uso</p></td>
<td align="left"><p>Somente computadores</p></td>
<td align="left"><p>Essa configuração de Política de Grupo habilita uma notificação na área de notificação que aparece quando o UE-V</p>
<p>o agente é executado pela primeira vez.</p></td>
<td align="left"><p>O padrão está habilitado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ping do local de armazenamento de configurações antes da sincronização</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política permite que a configuração do provedor de sincronização UE-V ping o caminho de armazenamento de configurações antes de tentar sincronizar as configurações para verificar a conexão.</p></td>
<td align="left"><p>Habilitar ou desabilitar essa configuração de Política de Grupo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Limite de aviso de tamanho do pacote de configurações</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de Política de Grupo permite que você configure o Agente UE-V para relatar quando um tamanho de arquivo de pacote de configurações atingir um limite definido.</p></td>
<td align="left"><p>Especifique o limite preferencial para configurações de tamanhos de pacote em quilobytes (KB).</p>
<p>Por padrão, o Agente UE-V não tem um limite de tamanho de arquivo de pacote.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações de caminho de armazenamento</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de Política de Grupo configura onde as configurações do usuário devem ser armazenadas.</p></td>
<td align="left"><p>Insira um caminho UNC (Convenção de Nomenização Universal) e variáveis como \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Caminho do catálogo de modelos de configurações</p></td>
<td align="left"><p>Somente computadores</p></td>
<td align="left"><p>Esta configuração de Política de Grupo configura onde os modelos de local de configurações personalizadas são armazenados. Essa configuração de política também configura se o catálogo deve ser usado para substituir os modelos padrão da Microsoft instalados pelo Agente UE-V.</p></td>
<td align="left"><p>Insira um caminho UNC (Convenção de Nomenização Universal), como \Server\TemplateShare ou um local de pasta no computador.</p>
<p>Marque a caixa de seleção para substituir os modelos padrão da Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações de sincronização em conexões com metros</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Esta configuração de Política de Grupo define se o UE-V sincroniza configurações em conexões com metros.</p></td>
<td align="left"><p>Por padrão, o Agente UE-V não sincroniza configurações em uma conexão com metros.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurações de sincronização sobre conexões com medidor mesmo quando o roaming</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Esta configuração de Política de Grupo define se o UE-V sincroniza configurações em conexões com metros fora da rede do provedor 1, por exemplo, quando a conexão de dados está no modo roaming.</p></td>
<td align="left"><p>Por padrão, o UE-V não sincroniza configurações em uma conexão com metros quando está no modo roaming.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tempo de tempo de sincronização</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Esta configuração de Política de Grupo configura o número de milissegundos que o computador aguarda antes de um tempo de espera quando recupera as configurações do usuário do local de configurações remotas. Se o local de armazenamento remoto não estiver disponível e o usuário não usar o provedor de sincronização, o início do aplicativo será adiado por esse número de milissegundos.</p></td>
<td align="left"><p>Especifique o tempo de tempo de sincronização preferencial em milissegundos. O valor padrão é 2000 milissegundos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizar configurações do Windows </p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de Política de Grupo configura a sincronização das configurações do Windows.</p></td>
<td align="left"><p>Selecione quais configurações do Windows sincronizam entre computadores.</p>
<p>Por padrão, temas do Windows, configurações de área de trabalho e configurações de Facilidade de Acesso sincronizam configurações entre computadores da mesma versão do sistema operacional.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ícone de bandeja</p></td>
<td align="left"><p>Somente computadores</p></td>
<td align="left"><p>Essa configuração de Política de Grupo habilita o ícone da bandeja UE-V.</p></td>
<td align="left"><p>O padrão está habilitado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usar a Virtualização da Experiência do Usuário (UE-V)</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de Política de Grupo permite habilitar ou desabilitar o UE-V.</p></td>
<td align="left"><p>Habilitar ou desabilitar essa configuração de Política de Grupo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuração VDI</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política configura a sincronização de informações de rebaixamento do UE-V para computadores em execução em um ambiente VDI em pool. Se essa política estiver habilitada, o estado de rebaixamento UE-V será copiado para o local de armazenamento de configurações no logout e restaurado no logon.</p></td>
<td align="left"><p>Habilitar ou desabilitar essa configuração de Política de Grupo.</p></td>
</tr>
</tbody>
</table>

 

**Observação**  
Além disso, as configurações da Política de Grupo estão disponíveis para muitos aplicativos da área de trabalho e aplicativos do Windows. Você pode usar essas configurações para habilitar ou desabilitar a sincronização de configurações para aplicativos específicos.

 

**Configurações da Política de Grupo de Aplicativos do Windows**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome da configuração da Política de Grupo</th>
<th align="left">Target</th>
<th align="left">Descrição da configuração da Política de Grupo</th>
<th align="left">Opções de configuração</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Não sincronizar aplicativos do Windows</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Esta configuração de Política de Grupo define se o Agente UE-V sincroniza configurações para aplicativos do Windows.</p></td>
<td align="left"><p>O padrão é sincronizar aplicativos do Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Lista de aplicativos do Windows</p></td>
<td align="left"><p>Computador e Usuário</p></td>
<td align="left"><p>Essa configuração lista os nomes de pacote da família dos aplicativos e estados do Windows expressamente se o UE-V sincroniza as configurações desse aplicativo.</p></td>
<td align="left"><p>Você pode usar essa configuração para especificar que as configurações de um aplicativo nunca são sincronizadas pelo UE-V, mesmo que as configurações de todos os outros aplicativos do Windows sejam sincronizadas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar aplicativos do Windows não listados</p></td>
<td align="left"><p>Computador e Usuário</p></td>
<td align="left"><p>Esta configuração de Política de Grupo define o comportamento de sincronização de configurações padrão do Agente UE-V para aplicativos Windows que não estão explicitamente listados na lista de aplicativos do Windows.</p></td>
<td align="left"><p>Por padrão, o Agente UE-V sincroniza apenas as configurações desses aplicativos do Windows incluídos na lista de aplicativos do Windows.</p></td>
</tr>
</tbody>
</table>

 

Para obter mais informações sobre como sincronizar aplicativos do Windows, consulte [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

**Para configurar configurações de Política de Grupo direcionadas ao computador**

1.  Use o Console de Gerenciamento de Política de Grupo (GPMC) ou o AgPM (Gerenciamento Avançado de Política de Grupo) no computador que atua como controlador de domínio para gerenciar configurações de Política de Grupo para computadores UE-V. Navegue **até Configuração do computador,** selecione **Políticas,** selecione **Modelos Administrativos,** clique em **Componentes**do Windows e selecione **Virtualização da Experiência do Usuário da Microsoft.**

2.  Selecione a configuração de Política de Grupo a ser editada.

**Para configurar configurações de Política de Grupo direcionadas ao usuário**

1.  Use o Console de Gerenciamento de Política de Grupo (GPMC) ou a ferramenta AgPM (Gerenciamento avançado de Política de Grupo) no Microsoft Desktop Optimization Pack (MDOP) no computador controlador de domínio para gerenciar as configurações de Política de Grupo para UE-V. Navegue **até Configuração do usuário,** selecione **Políticas,** selecione **Modelos Administrativos,** clique em **Componentes**do Windows e selecione **Virtualização da Experiência**do Usuário da Microsoft.

2.  Selecione a configuração de Política de Grupo editada.

O Agente UE-V usa a seguinte ordem de precedência para determinar a sincronização.

**Ordem de precedência para configurações do UE-V**

1.  Configurações direcionadas ao usuário gerenciadas pelas configurações da Política de Grupo - Essas configurações são armazenadas na chave do Registro pela Política de Grupo em `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Configurações direcionadas ao computador gerenciadas pelas configurações da Política de Grupo - Essas configurações são armazenadas na chave do Registro pela Política de Grupo em `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Configurações definidas pelo usuário atual usando Windows PowerShell ou Instrumentação de Gerenciamento do Windows (WMI) - Essas configurações são armazenadas pelo Agente UE-V neste local do Registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Configurações definidas para o computador usando Windows PowerShell ou WMI. Essas configurações são armazenadas pelo Agente UE-V neste local do Registro: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .

    **Tem uma sugestão para UE-V?** Adicione ou vote em sugestões [aqui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Tem um problema UE-V?** Use o [Fórum do TechNet UE-V.](https://social.technet.microsoft.com/Forums/home?forum=mdopuev)

## <a name="related-topics"></a>Tópicos relacionados


[Administrando o UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

[Gerenciar as configurações da UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
