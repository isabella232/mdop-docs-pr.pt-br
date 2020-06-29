---
title: Sincronização do Office 2013 com UE-V 2,0
description: Sincronização do Office 2013 com UE-V 2,0
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799962"
---
# Sincronização do Office 2013 com UE-V 2,0


O Microsoft User Experience Virtualization (UE-V) 2,0 dá suporte à sincronização da configuração do aplicativo Microsoft Office 2013 usando um modelo disponível na Galeria de modelos do UE-V. A combinação do suporte do Microsoft UE-V 2 e do App-V 5,0 SP2 do Office 2013 Professional Plus permite a mesma experiência na instância virtualizada do Office 2013 a partir de qualquer dispositivo habilitado para UE-V ou área de trabalho virtualizada.

Para ativar o suporte para configurações de aplicativo do UE-V do Office 2013, você pode baixar modelos oficiais do Office 2013 oficiais da [Microsoft User Experience Virtualization (UE-v) 2 template gallery](https://go.microsoft.com/fwlink/p/?LinkId=246589). Esse recurso fornece modelos de localização de configurações do UE-V criadas pela Microsoft e também modelos de localização de configurações desenvolvidos pela Comunidade.

## Suporte do Microsoft Office no UE-V


O UE-V 1,0 e o UE-V 2 incluem modelos de local de configurações para o Microsoft Office 2010. Esses modelos são distribuídos e registrados como parte do processo de instalação do UE-V Agent. Esses modelos ajudam a sincronizar a experiência do Office dos usuários entre dispositivos. Os modelos UE-V para Office 2013 fornecem uma experiência de configurações muito semelhante aos modelos do Office 2010. As configurações do Microsoft Office 2013 em roaming pela experiência do Office 365 não estão incluídas nessas configurações. Para obter uma lista das configurações específicas do Office 365, consulte [visão geral das configurações de roaming e de usuário do office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).

## Configurações do Office 2013 sincronizadas


As tabelas a seguir contêm os detalhes do suporte do Office 2013 no UE-V:

### Modelos do UE-V suportados para Microsoft Office

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Modelos do Office 2013 (UE-V 2,0, disponíveis na Galeria UE-V):</th>
<th align="left">Modelos do Office 2010 (UE-V 1,0 &amp; 1,0 SP1):</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftOffice2013Win32.xml</p>
<p>MicrosoftOffice2013Win64.xml</p>
<p>MicrosoftLync2013Win32.xml</p>
<p>MicrosoftLync2013Win64.xml</p></td>
<td align="left"><p>MicrosoftOffice2010Win32.xml</p>
<p>MicrosoftOffice2010Win64.xml</p>
<p>MicrosoftLync2010.xml</p>
<p></p></td>
</tr>
</tbody>
</table>

 

### Aplicativos do Microsoft Office com suporte nos modelos UE-V

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Access 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft Word 2013</p>
<p>Gerenciador de carregamento do Microsoft Office</p></td>
<td align="left"><p>Microsoft Access 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft SharePoint Designer 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft Word 2010</p>
<p></p></td>
</tr>
</tbody>
</table>

 

## Implantando os modelos do Office 2013


Você pode implantar o modelo de local de configurações do UE-V com os seguintes métodos:

-   **Registrando o modelo via PowerShell**. Se você usar o Windows PowerShell para gerenciar computadores, execute o seguinte comando do Windows PowerShell aberto como administrador para registrar esse modelo de local de configurações:

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    Para obter mais informações sobre o uso do UE-V e do Windows PowerShell, consulte [Gerenciando modelos de localização de configurações do UE-v 2. x usando o Windows PowerShell e o WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

-   **Registrando o modelo via caminho de catálogo de modelos**. Se você usar o caminho do catálogo de modelos de configurações para gerenciar modelos nos computadores dos usuários, copie o modelo do Office 2013 para a pasta definida no UE-V Agent. Na próxima vez que a tarefa agendada de atualização automática de modelo (ApplySettingsCatalog.exe) for executada, o modelo de local de configurações será registrado no dispositivo. Para obter mais informações, consulte [implantando o catálogo de modelos de configurações para UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).

-   **Registrando o modelo via Configuration Manager**. Se você usar o Configuration Manager para gerenciar seus modelos de armazenamento de configurações do UE-V, recrie o CAB de linha de base do modelo, importe-o para o Configuration Manager e, em seguida, implante a linha de base para seus clientes. Para obter mais informações, consulte as diretrizes fornecidas na documentação do [pacote de configuração do System Center 2012 para o Microsoft User Experience Virtualization 2](https://go.microsoft.com/fwlink/?LinkId=317263).






 

 





