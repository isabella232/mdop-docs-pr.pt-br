---
title: Como carregar uma imagem do MED-V no servidor
description: Como carregar uma imagem do MED-V no servidor
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799725"
---
# Como carregar uma imagem do MED-V no servidor


Depois que uma imagem do MED-V tiver sido testada, ela poderá ser empacotada e, em seguida, carregada para o servidor. Para obter informações sobre como configurar um servidor de distribuição da Web Image, consulte [como configurar o servidor de distribuição da Web de imagem](how-to-configure-the-image-web-distribution-server.md).

Depois que uma imagem do MED-V é compactada e carregada no servidor, ela pode ser distribuída aos usuários usando um centro de distribuição de software corporativo ou pode ser baixada pelos usuários que usam um pacote de implantação. Para obter informações sobre a implantação usando um centro de distribuição de software corporativo, consulte [implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software corporativo](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md). Para obter informações sobre a implantação usando um pacote, consulte [implantando um espaço de trabalho do MED-V usando um pacote de implantação](deploying-a-med-v-workspace-using-a-deployment-package.md).

**Observação**  
Antes de carregar uma imagem, verifique se um proxy da Web não está definido nas configurações do navegador e se o Windows Update não está em execução no momento.



**Para carregar uma imagem do MED-V para o servidor**

1.  No painel **imagens compactadas locais** , selecione a imagem que você criou.

2.  Clique em **carregar**.

    A imagem é carregada no servidor. Isso pode demorar um pouco.

    As imagens no servidor são definidas com as propriedades listadas na tabela a seguir.

**Imagens compactadas nas propriedades do servidor**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriedade</th>
<th align="left">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome da imagem</p></td>
<td align="left"><p>O nome da imagem empacotada conforme definido quando o administrador criou a imagem.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versão</p></td>
<td align="left"><p>A versão da imagem exibida.</p>
<div class="alert">
<strong>Observação</strong><br/><p>Todas as versões anteriores são mantidas, a menos que sejam excluídas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Tamanho do arquivo (compactado)</p></td>
<td align="left"><p>O tamanho compactado físico da imagem.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tamanho da imagem (não compactado)</p></td>
<td align="left"><p>O tamanho físico não compactado da imagem.</p></td>
</tr>
</tbody>
</table>



## Tópicos relacionados


[Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Usando a interface de usuário do Console de Gerenciamento do MED-V](using-the-med-v-management-console-user-interface.md)

[Criando uma imagem do Virtual PC para o MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Como empacotar uma imagem do MED-V](how-to-pack-a-med-v-image.md)









