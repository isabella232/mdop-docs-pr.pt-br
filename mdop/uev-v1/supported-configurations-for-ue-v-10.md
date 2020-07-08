---
title: Configurações com suporte para a UE-V 1.0
description: Configurações com suporte para a UE-V 1.0
author: dansimp
ms.assetid: d90ab83e-741f-48eb-b1d8-a64cb9259f7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a84514317de8a4cfd9df9c94a9a130933b00874a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799695"
---
# Configurações com suporte para a UE-V 1.0


O Microsoft User Experience Virtualization (UE-V) suporta as seguintes configurações descritas.

**Observação**  A Microsoft oferece suporte para o Service Pack atual e, em alguns casos, o Service Pack anterior. Para localizar os cronogramas de suporte para o seu produto, consulte os [pacotes de serviço com suporte do ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obter mais informações sobre a política de ciclo de vida do suporte da Microsoft, consulte [perguntas frequentes sobre a política de suporte ao ciclo](https://go.microsoft.com/fwlink/p/?LinkId=31976)

 

## Configurações compatíveis para o UE-V Agent e o UE-V Generator


A tabela a seguir lista os sistemas operacionais que dão suporte ao gerador de virtualização da experiência do usuário e o agente de virtualização da experiência do usuário.

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
<th align="left"><strong>Sistema operacional</strong></th>
<th align="left"><strong>Edição</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Arquitetura do sistema</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Ultimate, Enterprise ou Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (Generator)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Padrão, corporativo, Data Center ou servidor Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (Generator)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Enterprise ou Professional Edition</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>32 bits ou 64 bits</p></td>
<td align="left"><p>.NET Framework 4 ou .NET Framework 3,5 SP1 (agente)</p>
<p>.NET Framework 4 (Generator)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Padrão ou Datacenter</p></td>
<td align="left"><p>Nenhum(a)</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>.NET Framework 4 ou .NET Framework 3,5 SP1 (agente)</p>
<p>.NET Framework 4 (Generator)</p></td>
</tr>
</tbody>
</table>

 

Não há nenhum requisito especial de RAM específico para o UE-V.

A instalação do UE-V Agent exige direitos administrativos e exigirá que o computador seja reiniciado antes que o UE-V Agent possa ser executado.

**Importante**  O recurso sincronizar suas configurações no Windows 8 deve ser desabilitado para permitir que o UE-V funcione corretamente. A sincronização de configurações com o Windows 8 e a UE-V resultará em um comportamento de sincronização imprevisível.

 

### <a href="" id="requirements-for-the-offline-files-feature-"></a>Requisitos para o recurso arquivos offline

O UE-V Agent pode sincronizar as configurações de usuário para computadores que não estão sempre conectados à rede corporativa, como um computador laptop ou computadores localizados em escritórios remotos, bem como computadores que estejam sempre conectados à rede corporativa, como servidores Windows que hospedam sessões da interface de área de trabalho virtual (VDI).

A configuração padrão do UE-V usa o recurso de arquivo offline do Windows para sincronizar as configurações. Os arquivos offline garantem que as configurações do usuário estejam disponíveis mesmo quando o computador deixar a rede da empresa. Todas as alterações feitas nas configurações são sincronizadas automaticamente com o local de armazenamento de configurações quando a conexão com a rede da empresa é restabelecida. Os arquivos offline também garantem que as configurações do usuário estejam disponíveis para computadores localizados em um escritório remoto com uma conexão lenta ou limitada.

Para sincronizar as configurações de computadores que eventualmente deixam a rede empresarial, o recurso arquivos offline deve ser habilitado e iniciado antes de a implantação do UE-V Agent começar. O recurso arquivos offline está habilitado por padrão no Windows7. O recurso é desabilitado por padrão no Windows Server2008R2, no Windows Server 2012 e no Windows 8. Se o recurso de arquivos offline não estiver habilitado, a sincronização das configurações do UE-V não será bem-sucedida.

-   **Windows 7**

    O recurso arquivos offline está habilitado por padrão no Windows 7. Se necessário, os arquivos offline podem ser habilitados usando o seguinte comando em um prompt de comando elevado:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows 8**

    O recurso arquivos offline está desabilitado por padrão na versão do Windows 8. Os arquivos offline podem ser habilitados no Windows 8 usando o seguinte comando em um prompt de comando elevado:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows Server 2008 R2 e Windows Server 2012**

    O recurso arquivos offline não é instalado por padrão no Windows Server 2008 R2 ou no Windows Server 2012. Para habilitar o recurso arquivos offline, o pacote de experiência da área de trabalho deve ser instalado. Esse é um componente de servidor opcional que inclui o recurso arquivos offline. Depois de instalado, inicie o recurso arquivos offline com os seguintes comandos em um prompt de comando elevado:

    ``` syntax
    sc config csc start= system
    ```

    ``` syntax
    sc config cscservice start= auto
    ```

O computador deve ser reinicializado para que as configurações comecem a sincronizar.

### Sincronização para computadores com conexões sempre disponíveis

Quando você usa o UE-V em computadores que estão sempre conectados à rede corporativa, como um computador Windows Server que hospeda sessões de VDI, os arquivos offline devem ser desabilitados.

Quando o UE-V Agent está configurado para sincronizar as configurações sem usar arquivos offline, o servidor de armazenamento de configurações é tratado como um compartilhamento de rede padrão. As configurações são sincronizadas quando a rede está disponível. Nesta configuração, o UE-V Agent pode ser configurado para dar uma notificação se a importação das configurações do aplicativo for adiada.

Se o recurso de arquivos offline não for usado, você deve desabilitar o comportamento padrão do UE-V antes ou durante a implantação do UE-V Agent. Para desativar os arquivos offline para UE-V, siga um destes procedimentos:

-   Antes de implantar o UE-V Agent, marque a caixa de seleção "não usar arquivos offline" na configuração da política de grupo UE-V.

-   Durante a instalação do UE-V, defina o parâmetro AgentSetup.exe `SyncMethod = None` no prompt de comando ou em um arquivo em lotes. Para obter mais informações sobre como implantar o agente, consulte [implantando o UE-V Agent](deploying-the-ue-v-agent.md).

Se você desabilitar a configuração de arquivos offline para UE-V e não especificar o parâmetro **SyncMethod** no momento da instalação, a instalação do UE-v Agent falhará. Você também pode desativar os arquivos offline com o PowerShell ou o WMI. Para obter mais informações sobre os comandos do WMI e do PowerShell, consulte [Gerenciando o agente do UE-V 1,0 e pacotes com o PowerShell e o WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

O computador deve ser reinicializado para que as configurações comecem a sincronizar.

### Pré-requisitos para o recurso do PowerShell do UE-V

O recurso do PowerShell do UE-V do agente exige que o .NET Framework versão 3,5 SP1 seja habilitado e PowerShell versão 2,0 ou superior.

### Pré-requisitos para suporte ao gerador do UE-V

Instale o UE-V Generator no computador que é usado para criar modelos de local de configurações personalizadas. Esse computador deve ter os aplicativos instalados cujas configurações serão transferidas para o roaming. Você deve ser membro do grupo Administradores no computador que executa o software do gerador do UE-V. Além disso, o UE-V Generator deve ser instalado em um computador que usa um sistema de arquivos NTFS. O software do gerador do UE-V requer o .NET Framework versão 4. Para obter mais informações, consulte [planejando a implantação de modelos personalizados para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Tópicos relacionados


[Planejamento para a UE-V 1.0](planning-for-ue-v-10.md)

[Como preparar seu ambiente para a UE-V](preparing-your-environment-for-ue-v.md)

[Implantação da UE-V 1.0](deploying-ue-v-10.md)

Configurações com suporte para a virtualização da experiência do usuário [implantando o local de armazenamento de configurações para UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Instalação do gerador da UE-V](installing-the-ue-v-generator.md)

[Implantação do agente da UE-V](deploying-the-ue-v-agent.md)

 

 





