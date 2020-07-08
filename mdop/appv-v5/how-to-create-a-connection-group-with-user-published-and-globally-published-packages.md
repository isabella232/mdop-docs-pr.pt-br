---
title: Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados
description: Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796478"
---
# Como criar um grupo de conexão com pacotes publicados pelo usuário e globalmente publicados
Você pode criar grupos de conexão intitulados pelo usuário que contenham pacotes publicados pelo usuário e publicados globalmente, usando um dos seguintes métodos:

-   [Como usar cmdlets do PowerShell para criar grupos de conexão qualificados pelo usuário](#bkmk-posh-userentitled-cg)

-   [Como usar o servidor do App-V para criar grupos de conexão qualificados pelo usuário](#bkmk-appvserver-userentitled-cg)

**O que saber antes de começar:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cenários sem suporte e possíveis problemas</th>
<th align="left">Resultado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Você não pode incluir pacotes publicados pelo usuário em grupos de conexão habilitados globalmente.</p></td>
<td align="left"><p>O grupo de conexão falhará.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Se você publicar um pacote globalmente e, em seguida, criar um grupo de conexões publicada pelo usuário no qual você fez esse pacote não opcional, ainda poderá executar <strong> &lt; o AppvClientPackage Package &gt; -global </strong> para cancelar a publicação do pacote, mesmo quando esse pacote estiver sendo usado em outro grupo de conexão.</p></td>
<td align="left"><p>Se qualquer outro grupo de conexão estiver usando esse pacote, o pacote irá falhar nesses grupos de conexão.</p>
<p>Para evitar a publicação inadvertida de um pacote não opcional que está sendo usado em outro grupo de conexão, recomendamos que você acompanhe os grupos de conexão em que usou um pacote não opcional.</p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**Como usar cmdlets do PowerShell para criar grupos de conexão intitulados pelo usuário**

1.  Para adicionar e publicar pacotes, use os seguintes comandos:

    **Add-AppvClientPackage package1 \ _AppV \ _file \ _Path**

    **Add-AppvClientPackage Package2 \ _AppV \ _file \ _Path**

    **Publish-AppvClientPackage-PackageID package1 \ _ID-VersionId package1 \ _Version ID-global**

    **Publish-AppvClientPackage-PackageID Package2 \ _ID-VersionIdPackage2-\ _ID**

2.  Crie o arquivo XML do grupo de conexão. Para obter mais informações, consulte [sobre o arquivo de grupo de conexão](about-the-connection-group-file.md).

3.  Adicione e publique o grupo de conexão usando os seguintes comandos:

    **Conexão Add-AppvClientConnectionGroup \ _Group \ _XML \ _file \ _Path**

    **Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-VersionId CG \ _Version \ _ID**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**Como usar o servidor do App-V para criar grupos de conexão intitulados pelo usuário**

1.  Abra o console de gerenciamento do App-V 5,0.

2.  Siga as instruções em [como publicar um pacote usando o console de gerenciamento](how-to-publish-a-package-by-using-the-management-console-50.md) para publicar pacotes globalmente e para o usuário.

3.  Siga as instruções em [como criar um grupo de conexão](how-to-create-a-connection-group.md) para criar o grupo de conexões e adicionar os pacotes publicados pelo usuário e publicados globalmente.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Gerenciando grupos de conexão](managing-connection-groups.md)

[Como usar pacotes opcionais em grupos de conexão](how-to-use-optional-packages-in-connection-groups.md)

 

 





