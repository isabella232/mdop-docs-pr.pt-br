---
title: Implantação do agente da UE-V
description: Implantação do agente da UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800021"
---
# Implantação do agente da UE-V


O Microsoft User Experience Virtualization (UE-V) Agent deve ser executado em cada computador que usa o UE-V para transferir o aplicativo e as configurações do Windows. Um único arquivo de instalação, AgentSetup.exe, instala o UE-V Agent nos sistemas operacionais de 32 bits e 64 bits. Os parâmetros de linha de comando do UE-V Agent são os seguintes:

**Parâmetros de linha de comando AgentSetup.exe**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Parâmetro de linha de comando</strong></th>
<th align="left"><strong>Definição</strong></th>
<th align="left"><strong>Observações</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help ou/h ou/?</p></td>
<td align="left"><p>Exibe a caixa de diálogo AgentSetup.exe uso.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Indica o caminho UNC (Convenção Universal de nomenclatura) que define onde as configurações são armazenadas.</p></td>
<td align="left"><p>as variáveis de ambiente% username% ou% computernamename% são aceitas. O script pode exigir variáveis de escape.</p>
<p><strong>Padrão </strong> : &lt; nenhum &gt; (Active Directory User Home)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Indica o caminho UNC (Convenção Universal de nomenclatura) que define o local verificado para novos modelos de local de configurações.</p></td>
<td align="left"><p>Só é necessário para modelos de local de configurações personalizadas</p></td>
</tr>
<tr class="even">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Especifica se os modelos padrão da Microsoft devem ser registrados durante a instalação.</p></td>
<td align="left"><p>Verdadeiro | Falsas</p>
<p><strong>Padrão </strong> : verdadeiro</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncMethod</p></td>
<td align="left"><p>Especifica qual método de sincronização deve ser usado.</p></td>
<td align="left"><p>OfflineFiles | Nenhuma</p>
<p><strong>Padrão </strong> : OfflineFiles</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Especifica o número de milissegundos que o computador aguarda antes do tempo limite quando ele recupera as configurações de usuário do local de armazenamento de configurações.</p></td>
<td align="left"><p><strong>Padrão </strong> : 2000 milissegundos</p>
<p>(Aguarde até 2 segundos)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Especifica se a sincronização de UE-V está habilitada ou desabilitada.</p></td>
<td align="left"><p>Verdadeiro | Falsas</p>
<p><strong>Padrão </strong> : verdadeiro</p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Especifica um tamanho de arquivo de pacote de configurações em bytes quando o UE-V Agent informa que os arquivos excedem o limite.</p></td>
<td align="left"><p>&lt;tamanho&gt;</p>
<p><strong>Padrão </strong> : nenhum (sem limite de aviso)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Especifica a configuração de participação no programa de aperfeiçoamento da experiência do usuário. Se definido como true, as informações do instalador serão carregadas no site do programa de aperfeiçoamento da experiência do usuário da Microsoft. Se definido como false, nenhuma informação será carregada.</p></td>
<td align="left"><p>Verdadeiro | Falsas</p>
<p><strong>Padrão </strong> : falso</p>
<p><strong>No Windows 7 </strong> : verdadeiro</p></td>
</tr>
</tbody>
</table>

 

Durante a instalação, o parâmetro de linha de comando SettingsStoragePath especifica o local de armazenamento de configurações para os valores de configurações. Um local de armazenamento de configurações pode ser definido antes da implantação do UE-V Agent. Se nenhuma localização de armazenamento de configurações estiver definida, o UE-V usará o diretório inicial de usuário do Active Directory como o local de armazenamento de configurações. Ao especificar a configuração SettingsStoragePath durante a configuração e usar o% username% como parte do valor, isso fará o roaming da mesma experiência de configurações do usuário em todos os computadores ou sessões nos quais um usuário faz logon. Se você especificar as variáveis%username%\\%ComputerName% como parte do valor SettingsStoragePath, isso irá preservar a experiência de configurações para cada computador.

Os arquivos do Windows Installer (. msi) específicos da arquitetura são fornecidos para a instalação do UE-V Agent, além do instalador combinado de 32 bits e 64 bits. Os arquivos de instalação do AgentSetupx86.msi ou AgentSetupx64.msi são menores do que o arquivo AgentSetup.exe e podem simplificar as implantações do agente. Os parâmetros de linha de comando para o instalador do AgentSetup.exe são suportados para a instalação do Windows Installer (. msi).

**Observação**  Durante a instalação ou desinstalação do agente do UE-V, você pode usar o arquivo AgentSetup.exe ou &lt; o &gt; arquivo AgentSetup Arch. msi, mas não ambos. O mesmo arquivo deve ser usado para desinstalar o UE-V Agent, pois foi usado para instalar o UE-V Agent.

 

Certifique-se de usar o formato de variável correto ao instalar o UE-V Agent. A tabela a seguir fornece exemplos de opções de implantação para usar os arquivos de instalação do AgentSetup.exe ou do Windows Installer (. msi).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Tipo de implementação</strong></th>
<th align="left"><strong>Descrição da implantação</strong></th>
<th align="left"><strong>Exemplo</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Prompt de comando</p></td>
<td align="left"><p>Ao instalar o UE-V Agent a partir de um prompt de comando, use o formato de variável% ^ username%. Se forem necessárias aspas por causa de espaços no caminho de armazenamento de configurações, use um arquivo de script em lotes para implantação.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Script em lotes</p></td>
<td align="left"><p>Ao instalar o UE-V Agent a partir de um arquivo de script em lotes, use o formato de variável%% username%%. Se você usar esse método de instalação, deverá escapar a variável com os caracteres%%. Sem esse caractere, o script expande a variável username no tempo de instalação, em vez do tempo de execução, fazendo com que o UE-V use um único local de armazenamento de configurações para todos os usuários.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Ao instalar o UE-V Agent a partir de um prompt do PowerShell ou de um script do PowerShell, use o formato de variável% username%.</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribuição de software eletrônico, como a implantação da implantação de software do Configuration Manager)</p></td>
<td align="left"><p>Ao instalar o UE-V Agent com o Configuration Manager, use o formato de variável ^% username ^%.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

**Observação**  A instalação do agente U-VA exige direitos de administrador, e o computador exigirá uma reinicialização antes que o UE-V Agent possa ser executado.

 

## Métodos de implantação do agente do UE-V em um compartilhamento de rede


Você pode usar os seguintes métodos para implantar o UE-V Agent:

-   Uma solução ESD (Electronic Software Distribution) que pode instalar um arquivo Windows Installer (. msi).

-   Um script de instalação que faz referência ao arquivo do Windows Installer (. msi) que está armazenado centralmente em um compartilhamento.

-   Executar manualmente o programa de instalação no computador.

Para implantar o UE-V Agent a partir de um compartilhamento de rede, use as seguintes etapas:

**Para instalar e configurar o UE-V Agent a partir de um compartilhamento de rede**

1.  Testar o arquivo de instalação do agente do UE-V (AgentSetup.exe) em um compartilhamento de rede ao qual os usuários têm permissão "ler".

2.  Implante um script para os computadores dos usuários que instalam o UE-V Agent. O script deve especificar o local de armazenamento de configurações.

**Atualize o UE-V Agent**

As atualizações do software de agente UE-V serão fornecidas por meio do Microsoft Update. Durante uma atualização do UE-V Agent, o grupo padrão de modelos de localização de configurações para aplicativos e configurações do Windows comuns podem ser atualizados. As atualizações do UE-V Agent podem ser implantadas usando a infraestrutura ESD (Enterprise Software Distribution).

## Tópicos relacionados


[Implantação da UE-V 1.0](deploying-ue-v-10.md)

[Configurações com suporte para a UE-V 1.0](supported-configurations-for-ue-v-10.md)

[Implantação da localização do armazenamento de configurações para a UE-V 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Instalação do gerador da UE-V](installing-the-ue-v-generator.md)

Implantar o agente de virtualização da experiência do usuário
 

 





