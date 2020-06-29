---
title: Como fazer upgrade de um aplicativo virtual usando a linha de comando
description: Como fazer upgrade de um aplicativo virtual usando a linha de comando
author: dansimp
ms.assetid: 83c97767-6ea1-42aa-b411-ccc9fa61cf81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8612deb31a1692dd85cfee88ca4b18cbc5ac2ab2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796930"
---
# Como fazer upgrade de um aplicativo virtual usando a linha de comando


Use o procedimento a seguir para atualizar um aplicativo virtual usando uma linha de comando.

**Para atualizar um aplicativo virtual**

1.  No computador que está executando o sequenciador do Application Virtualization (App-V), para abrir o prompt de comando, selecione **Iniciar**, **executar**e digite **cmd**. Clique em **OK**.

2.  No prompt de comando, especifique o local em que o sequenciador do App-V está instalado. Por exemplo, no prompt de comando, você pode digitar o seguinte: **CD c:\\Arquivos de Files\\Microsoft Application Virtualization Sequencer**.

3.  No prompt de comando, digite o seguinte comando, substituindo o texto entre aspas pelos valores:

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Observação**  
    Você pode especificar parâmetros adicionais usando a linha de comando, dependendo da complexidade do aplicativo que está atualizando. Para obter uma lista completa de parâmetros disponíveis para uso com o sequenciador App-V, consulte [parâmetros de linha de comando do sequenciador](sequencer-command-line-parameters.md).



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Pressione **Enter**.

## Tópicos relacionados


[Como criar ou atualizar aplicativos virtuais usando o sequenciador App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[Códigos de erro de linha de comando do Sequencer](sequencer-command-line-error-codes.md)

[Parâmetros de linha de comando do Sequencer](sequencer-command-line-parameters.md)









