---
title: Como configurar o cliente para recuperação de pacote de aplicativo
description: Como configurar o cliente para recuperação de pacote de aplicativo
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797203"
---
# Como configurar o cliente para recuperação de pacote de aplicativo


Quando o cliente está configurado com um servidor de gerenciamento do App-V (App-V) como seu servidor de publicação, por padrão no próximo ciclo de atualização de publicação, o cliente recupera do servidor o descritor de software aberto (OSD) e os arquivos de manifesto do pacote para cada pacote que o usuário está autorizado a usar. O cliente usa as informações de origem do pacote definidas nesses arquivos para determinar onde encontrar o conteúdo do pacote, os ícones e associações de tipo de arquivo.

Se você quiser que o cliente obtenha o conteúdo do pacote (arquivo SFT) de um servidor de streaming do App-V local ou outra fonte alternativa, como um servidor da Web ou um servidor de arquivos, em vez do servidor de gerenciamento do App-V, você pode configurar o valor da chave do registro ApplicationSourceRoot no computador para apontar para o compartilhamento de conteúdo local no outro servidor. O arquivo OSD ainda define o caminho de origem original para o conteúdo do pacote. No entanto, o cliente usa o valor da configuração ApplicationSourceRoot no lugar do servidor e do compartilhamento especificados no caminho do conteúdo no arquivo OSD. Isso redireciona o cliente para recuperar o conteúdo do outro servidor.

Você também pode configurar os valores da chave do registro OSDSourceRoot e IconSourceRoot se quiser substituir essas configurações no arquivo de manifesto do pacote ou nos caminhos enviados por um servidor de publicação. O OSDSourceRoot especifica um local de origem para a recuperação de arquivo OSD para um pacote de aplicativo durante a publicação. O IconSourceRoot especifica um local de origem para a recuperação de ícone para um pacote de aplicativo durante a publicação.

**Observação**  
-   As configurações de IconSourceRoot e OSDSourceRoot substituem os valores no arquivo de manifesto do pacote, portanto, se você tentar implantar um pacote usando o método de arquivo do Windows Installer (. msi), ele também substituirá os valores no arquivo de manifesto do pacote contido nesse arquivo. msi.

-   Durante as operações de streaming e de transmissão HTTP (S), os clientes do App-V 4,5 SP1 usam as configurações de servidor proxy configuradas no Internet Explorer no computador do usuário.



**Para configurar o valor da chave do registro ApplicationSourceRoot**

-   Configure o ApplicationSourceRoot no seguinte valor da chave do registro com um caminho UNC ou uma URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot

    O formato correto para o caminho UNC (Convenção de nomenclatura universal) é **\\\\computername\\sharefolder\\\ [pasta \] \ [\ \ \]**, em que a **pasta** é opcional. O **ComputerName** pode ser um FQDN (nome de domínio totalmente qualificado) ou um endereço IP, e **ShareFolder** pode ser uma letra de unidade. Somente a parte **\\\\computername\\sharedfolder** ou letra da unidade do caminho OSD é substituída.

    O formato correto para o caminho da URL é protocolo: a partir de **: \ [porta \] \ [/path\] \ [/\]**, em que a **porta** e o **caminho** são opcionais. Se **porta** não for especificada, será usada a porta padrão do protocolo. Somente a porção **Protocol://Server: Port** da URL OSD é substituída.

    **Importante**  
    Não há suporte para variáveis de ambiente na definição ApplicationSourceRoot.



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**Para configurar o valor de OSDSourceRoot**

-   Configure o OSDSourceRoot no seguinte valor da chave do registro com um caminho UNC ou uma URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot

    Os formatos aceitáveis para o OSDSourceRoot incluem caminhos e URLs UNC, como no exemplo a seguir:

    **\\\\computername\\sharefolder\\resource** ou **\\\\computername\\content** ou ** &lt; unidade &gt; : \\foldername**

    **http://computername/productivity/** or**https://computername/productivity/**

**Para configurar o valor de IconSourceRoot**

-   Configure o IconSourceRoot no seguinte valor da chave do registro com um caminho UNC ou uma URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot

    Os formatos aceitáveis para o IconSourceRoot incluem caminhos e URLs UNC, como no exemplo a seguir:

    **\\\\computername\\sharefolder\\resource** ou **\\\\computername\\content** ou ** &lt; unidade &gt; : \\foldername**

    **http://computername/productivity/** or**https://computername/productivity/**

## Tópicos relacionados


[Como definir as configurações de Registro do cliente do App-V usando a linha de comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









