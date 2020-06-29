---
title: Configurando o UE-V com objetos de Política de Grupo
description: Configurando o UE-V com objetos de Política de Grupo
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799924"
---
# Configurando o UE-V com objetos de Política de Grupo


Algumas configurações da política de grupo do Microsoft User Experience Virtualization (UE-V Microsoft Virtualization) podem ser definidas para computadores e outras pessoas podem ser definidas para os usuários. As configurações da política de configuração do UE-V Agent podem ser definidas para computadores ou usuários. Para obter informações sobre como instalar os arquivos ADMX da política de grupo do UE-V, consulte [instalando os modelos ADMX da política de grupo UE-v](installing-the-ue-v-group-policy-admx-templates.md).

As seguintes configurações de política podem ser configuradas para UE-V:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nome da configuração de política</strong></p></td>
<td align="left"><p><strong>Target</strong></p></td>
<td align="left"><p><strong>Descrição da configuração de política</strong></p></td>
<td align="left"><p><strong>Opções de configuração</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Usar a User Experience Virtualization (UE-V)</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política permite habilitar ou desabilitar a virtualização da experiência do usuário (UE-V).</p></td>
<td align="left"><p>Habilitar ou desabilitar essa configuração de política.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Caminho de armazenamento de configurações</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política define onde as configurações de usuário serão armazenadas.</p></td>
<td align="left"><p>Fornecer um caminho e variáveis UNC (Convenção Universal de nomenclatura), como \Server\SettingsShare%username%.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Caminho do catálogo de modelos de configurações</p></td>
<td align="left"><p>Computadores apenas</p></td>
<td align="left"><p>Essa configuração de política define onde os modelos de localização de configurações personalizadas são armazenados. Essa configuração de política também define se o catálogo será usado para substituir os modelos padrão do Microsoft que são instalados com o UE-V Agent.</p></td>
<td align="left"><p>Forneça um caminho UNC (Convenção Universal de nomenclatura), como \Server\TemplateShare ou um local de pasta no computador.</p>
<p></p>
<p>Marque a caixa de seleção para substituir os modelos padrão da Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Não usar arquivos offline</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política permite que você defina se a UE-V usará o recurso arquivos offline do Windows. Essa configuração de política também permite que você habilite a notificação para ocorrer quando a importação das configurações do usuário é atrasada.</p></td>
<td align="left"><p>Para configurar o UE-V Agent para não usar arquivos offline, habilite essa configuração.</p>
<p></p>
<p>Especifique se as notificações devem ser fornecidas quando a importação de configurações está atrasada.</p>
<p></p>
<p>Especifique a duração do tempo em segundos a ser aguardada até que a notificação seja exibida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tempo limite de sincronização</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política configura o número de milissegundos que o computador aguarda antes do tempo limite ao recuperar as configurações de usuário do local de configurações remotas. Se o local do armazenamento remoto não estiver disponível, a inicialização do aplicativo será adiada por esse número de milissegundos.</p></td>
<td align="left"><p>Especifique o tempo limite de sincronização preferencial em milissegundos. O valor padrão de 2000 milissegundos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Limite de aviso de tamanho do pacote</p></td>
<td align="left"><p>Computadores e usuários</p></td>
<td align="left"><p>Essa configuração de política permite que você configure o UE-V Agent para relatar quando um tamanho de arquivo de pacote de configurações atingir um limite definido.</p></td>
<td align="left"><p>Especificado o limite preferencial para configurações de tamanhos de pacote em quilobytes.</p>
<p>Por padrão, o UE-V Agent não tem um limite de tamanho de arquivo de pacote.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurações de aplicativo de roaming</p></td>
<td align="left"><p>Somente usuários</p></td>
<td align="left"><p>Essa configuração de política define o roaming das configurações de usuário dos aplicativos.</p></td>
<td align="left"><p>Selecione as configurações do Windows que serão transferidas entre computadores.</p>
<p>Por padrão, as configurações do usuário de aplicativos com o modelo de configurações fornecidas pela UE-V são móveis entre computadores.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurações de roaming do Windows</p></td>
<td align="left"><p>Somente usuários</p></td>
<td align="left"><p>Essa configuração de política define o roaming das configurações do Windows.</p></td>
<td align="left"><p>Selecione quais aplicativos serão movidos entre computadores.</p>
<p>Por padrão, os temas do Windows são movidos entre computadores da mesma versão do sistema operacional. As configurações da área de trabalho do Windows e da facilidade de acesso não são roamas.</p></td>
</tr>
</tbody>
</table>

 

**Para configurar políticas direcionadas a computador**

1.  Use o GPMC (console de gerenciamento de política de grupo) ou o gerenciamento avançado de política de grupo (AGPM) no computador do controlador de domínio que gerencia a política de grupo para computadores UE-V. Navegue até **configuração do computador**, **selecione políticas**, selecione **modelos administrativos**, clique em **componentes do Windows**e selecione **virtualização da experiência do usuário da Microsoft**.

2.  Selecione a configuração de política a ser editada.

**Para configurar políticas direcionadas pelo usuário**

1.  Use o GPMC (console de gerenciamento de política de grupo) ou a ferramenta de gerenciamento avançado de política de grupo (AGPM) no Microsoft Desktop Optimization Pack (MDOP) no computador do controlador de domínio que gerencia a política de grupo para UE-V. Navegue até **configuração do usuário**, **selecione políticas**, selecione **modelos administrativos**, clique em **componentes do Windows**e selecione **virtualização da experiência do usuário da Microsoft**.

2.  Selecione a configuração de política editada.

O UE-V Agent usa a seguinte ordem de precedência para determinar a sincronização.

**Ordem de precedência para configurações de UE-V**

1.  Configurações direcionadas pelo usuário gerenciadas pela política de grupo-essas configurações são armazenadas na chave do registro por política de grupo em `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .

2.  Configurações direcionadas por computador gerenciadas pela política de grupo-essas configurações são armazenadas na chave do registro por política de grupo em `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .

3.  Configurações definidas pelo usuário atual usando o PowerShell ou o WMI-essas configurações são armazenadas pelo UE-V Agent sob este local de registro: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .

4.  Configurações definidas para o computador usando o PowerShell ou o WMI. Esses parâmetros de configuração são armazenados pelo UE-V Agent em `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .

## Tópicos relacionados


[Administração da UE-V 1.0](administering-ue-v-10.md)

[Operações para a UE-V 1.0](operations-for-ue-v-10.md)

 

 





