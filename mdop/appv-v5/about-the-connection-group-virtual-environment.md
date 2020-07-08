---
title: Sobre o ambiente Virtual do grupo de conexão
description: Sobre o ambiente Virtual do grupo de conexão
author: dansimp
ms.assetid: 535fa640-cbd9-425e-8437-94650a70c264
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bd93c9e7acbf7bbf3f9da506d5d95b8df09e1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796617"
---
# Sobre o ambiente Virtual do grupo de conexão


**Neste tópico:**

-   [Como a prioridade do pacote é determinada](#bkmk-pkg-priority-deter)

-   [Mesclando caminhos de pacote idênticos em um diretório virtual em grupos de conexão](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a>Como a prioridade do pacote é determinada


O ambiente virtual e seu estado atual são associados ao grupo de conexão, e não aos pacotes individuais. Se um pacote do App-V for removido do grupo de conexão, o estado que existia como parte do grupo de conexões não será migrado com o pacote.

Se o mesmo pacote for uma parte de dois grupos de conexão diferentes, você precisará indicar qual App-V do grupo de conexões deve usar. Por exemplo, você pode ter dois pacotes em um grupo de conexão que cada um deles define o mesmo valor DWORD do registro.

O grupo de conexões usado é baseado na ordem em que um pacote aparece dentro do documento XML do **AppConnectionGroup** :

-   O primeiro pacote tem a precedência mais alta.

-   O segundo pacote tem a segunda precedência mais alta.

Considere o seguinte exemplo de seção:

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

Suponha que o mesmo valor DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) esteja definido no primeiro e terceiro pacote, como:

-   Pacote 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5

-   Pacote 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10

Como o pacote 1 aparece primeiro, o ambiente virtual do AppConnectionGroup terá o valor DWORD único de 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5). Isso significa que os aplicativos virtuais do pacote 1, do pacote 2 e do pacote 3 verão o valor 5 quando consultarem o HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.

Outros recursos de ambiente virtual são resolvidos da mesma forma, mas o caso usual é que as colisões ocorram no registro.

## <a href="" id="bkmk-merged-root-ve-exp"></a>Mesclando caminhos de pacote idênticos em um diretório virtual em grupos de conexão


Se dois ou mais pacotes em um grupo de conexão contiverem caminhos de diretório idênticos, os caminhos serão mesclados em um único diretório virtual dentro do ambiente virtual do grupo de conexão. Essa mesclagem de caminhos permite que um aplicativo em um pacote Acesse arquivos que estão em um pacote diferente.

Quando você remove um pacote de um grupo de conexão, os aplicativos desse pacote removido não conseguem mais acessar os arquivos nos pacotes restantes do grupo de conexão.

A ordem em que o App-V procura o nome de um arquivo no grupo conexão é especificado pela ordem em que os pacotes do App-V estão listados no arquivo de manifesto do grupo de conexão.

O exemplo a seguir mostra a ordem e a relação de uma pesquisa de nome de arquivo em um grupo de conexão para **o pacote a e o** **pacote B**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Empacotar um</th>
<th align="left">Pacote B</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>C:\Windows\System32</p></td>
<td align="left"><p>C:\Windows\System32</p></td>
</tr>
<tr class="even">
<td align="left"><p>C:\AppTest</p></td>
<td align="left"><p>C:\AppTest</p></td>
</tr>
</tbody>
</table>

 

No exemplo acima, quando um aplicativo virtualizado tenta localizar um arquivo específico, o pacote A é pesquisado primeiro em busca de um caminho de arquivo correspondente. Se um caminho correspondente não for encontrado, o pacote B será pesquisado usando as seguintes regras de mapeamento:

-   Se um arquivo denominado **test.txt** existir na mesma hierarquia de pastas virtuais nos dois pacotes de aplicativos, o primeiro arquivo coincidente será usado.

-   Se um arquivo chamado **bar.txt** existir na hierarquia de pastas virtuais de um pacote de aplicativo, mas não no outro, o primeiro arquivo coincidente será usado.






## Tópicos relacionados


[Gerenciando grupos de conexão](managing-connection-groups.md)

 

 





