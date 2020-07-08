---
title: Como sequenciar um novo aplicativo usando a linha de comando
description: Como sequenciar um novo aplicativo usando a linha de comando
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796975"
---
# Como sequenciar um novo aplicativo usando a linha de comando


Você pode usar uma linha de comando para sequenciar um novo aplicativo. Usar uma linha de comando é útil quando você precisa criar um grande número de aplicativos virtuais ou quando precisa criar aplicativos sequenciados em uma base recorrente.

**Importante**  
O sequenciamento de linha de comando permite somente o sequenciamento padrão. Se precisar alterar as configurações de instalação padrão do aplicativo que você está sequenciando, você deve modificar manualmente o aplicativo virtual ou atualizar o aplicativo virtual usando o sequenciador Application Virtualization (App-V). Para obter mais informações sobre como atualizar um aplicativo virtual usando o sequenciador App-V, consulte [como atualizar um aplicativo virtual existente](how-to-upgrade-an-existing-virtual-application.md).



Use o procedimento a seguir para criar um aplicativo virtual usando a linha de comando.

**Para sequenciar um aplicativo usando a linha de comando**

1.  No computador que está executando o sequenciador App-V, abra o prompt de comando selecionando **Iniciar**, **executar**e, em seguida, digite **cmd**. Clique em **OK**.

2.  Use o prompt de comando para especificar o local de onde o sequenciador do App-V está instalado. Por exemplo, no prompt de comando, você pode digitar o seguinte: **CD c:\\Arquivos de Files\\Microsoft Application Virtualization Sequencer**.

3.  No prompt de comando, digite o seguinte comando, substituindo o texto entre aspas pelos valores:

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Observação**  
    Você pode especificar parâmetros adicionais usando a linha de comando, dependendo da complexidade do aplicativo que está sequenciando. Para obter uma lista completa de parâmetros disponíveis para uso com o sequenciador App-V, consulte [parâmetros de linha de comando do sequenciador](sequencer-command-line-parameters.md).



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
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
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









