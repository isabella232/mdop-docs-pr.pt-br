---
title: Sobre o ambiente Virtual do grupo de conexão
description: Sobre o ambiente Virtual do grupo de conexão
author: dansimp
ms.assetid: b7bb0e3d-8cd5-45a9-b84e-c9ab4196a18c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43f30c2100fc982170f15c305b03cd338b5d8afd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796611"
---
# <span data-ttu-id="92da7-103">Sobre o ambiente Virtual do grupo de conexão</span><span class="sxs-lookup"><span data-stu-id="92da7-103">About the Connection Group Virtual Environment</span></span>


**<span data-ttu-id="92da7-104">Neste tópico:</span><span class="sxs-lookup"><span data-stu-id="92da7-104">In this topic:</span></span>**

-   [<span data-ttu-id="92da7-105">Como a prioridade do pacote é determinada</span><span class="sxs-lookup"><span data-stu-id="92da7-105">How package priority is determined</span></span>](#bkmk-pkg-priority-deter)

-   [<span data-ttu-id="92da7-106">Mesclando caminhos de pacote idênticos em um diretório virtual em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="92da7-106">Merging identical package paths into one virtual directory in connection groups</span></span>](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a><span data-ttu-id="92da7-107">Como a prioridade do pacote é determinada</span><span class="sxs-lookup"><span data-stu-id="92da7-107">How package priority is determined</span></span>


<span data-ttu-id="92da7-108">O ambiente virtual e seu estado atual são associados ao grupo de conexão, e não aos pacotes individuais.</span><span class="sxs-lookup"><span data-stu-id="92da7-108">The virtual environment and its current state are associated with the connection group, not with the individual packages.</span></span> <span data-ttu-id="92da7-109">Se um pacote do App-V for removido do grupo de conexão, o estado que existia como parte do grupo de conexões não será migrado com o pacote.</span><span class="sxs-lookup"><span data-stu-id="92da7-109">If an App-V package is removed from the connection group, the state that existed as part of the connection group will not migrate with the package.</span></span>

<span data-ttu-id="92da7-110">Se o mesmo pacote for uma parte de dois grupos de conexão diferentes, você precisará indicar qual App-V do grupo de conexões deve usar.</span><span class="sxs-lookup"><span data-stu-id="92da7-110">If the same package is a part of two different connection groups, you have to indicate which connection group App-V should use.</span></span> <span data-ttu-id="92da7-111">Por exemplo, você pode ter dois pacotes em um grupo de conexão que cada um deles define o mesmo valor DWORD do registro.</span><span class="sxs-lookup"><span data-stu-id="92da7-111">For example, you might have two packages in a connection group that each define the same registry DWORD value.</span></span>

<span data-ttu-id="92da7-112">O grupo de conexões usado é baseado na ordem em que um pacote aparece dentro do documento XML do **AppConnectionGroup** :</span><span class="sxs-lookup"><span data-stu-id="92da7-112">The connection group that is used is based on the order in which a package appears inside the **AppConnectionGroup** XML document:</span></span>

-   <span data-ttu-id="92da7-113">O primeiro pacote tem a precedência mais alta.</span><span class="sxs-lookup"><span data-stu-id="92da7-113">The first package has the highest precedence.</span></span>

-   <span data-ttu-id="92da7-114">O segundo pacote tem a segunda precedência mais alta.</span><span class="sxs-lookup"><span data-stu-id="92da7-114">The second package has the second highest precedence.</span></span>

<span data-ttu-id="92da7-115">Considere o seguinte exemplo de seção:</span><span class="sxs-lookup"><span data-stu-id="92da7-115">Consider the following example section:</span></span>

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

<span data-ttu-id="92da7-116">Suponha que o mesmo valor DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) esteja definido no primeiro e terceiro pacote, como:</span><span class="sxs-lookup"><span data-stu-id="92da7-116">Assume that same DWORD value ABC (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region) is defined in the first and third package, such as:</span></span>

-   <span data-ttu-id="92da7-117">Pacote 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5</span><span class="sxs-lookup"><span data-stu-id="92da7-117">Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5</span></span>

-   <span data-ttu-id="92da7-118">Pacote 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10</span><span class="sxs-lookup"><span data-stu-id="92da7-118">Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=10</span></span>

<span data-ttu-id="92da7-119">Como o pacote 1 aparece primeiro, o ambiente virtual do AppConnectionGroup terá o valor DWORD único de 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5).</span><span class="sxs-lookup"><span data-stu-id="92da7-119">Since Package 1 appears first, the AppConnectionGroup's virtual environment will have the single DWORD value of 5 (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5).</span></span> <span data-ttu-id="92da7-120">Isso significa que os aplicativos virtuais do pacote 1, do pacote 2 e do pacote 3 verão o valor 5 quando consultarem o HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.</span><span class="sxs-lookup"><span data-stu-id="92da7-120">This means that the virtual applications in Package 1, Package 2, and Package 3 will all see the value 5 when they query for HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region.</span></span>

<span data-ttu-id="92da7-121">Outros recursos de ambiente virtual são resolvidos da mesma forma, mas o caso usual é que as colisões ocorram no registro.</span><span class="sxs-lookup"><span data-stu-id="92da7-121">Other virtual environment resources are resolved similarly, but the usual case is that the collisions occur in the registry.</span></span>

## <a href="" id="bkmk-merged-root-ve-exp"></a><span data-ttu-id="92da7-122">Mesclando caminhos de pacote idênticos em um diretório virtual em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="92da7-122">Merging identical package paths into one virtual directory in connection groups</span></span>


<span data-ttu-id="92da7-123">Se dois ou mais pacotes em um grupo de conexão contiverem caminhos de diretório idênticos, os caminhos serão mesclados em um único diretório virtual dentro do ambiente virtual do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="92da7-123">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span> <span data-ttu-id="92da7-124">Essa mesclagem de caminhos permite que um aplicativo em um pacote Acesse arquivos que estão em um pacote diferente.</span><span class="sxs-lookup"><span data-stu-id="92da7-124">This merging of paths allows an application in one package to access files that are in a different package.</span></span>

<span data-ttu-id="92da7-125">Quando você remove um pacote de um grupo de conexão, os aplicativos desse pacote removido não conseguem mais acessar os arquivos nos pacotes restantes do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="92da7-125">When you remove a package from a connection group, the applications in that removed package are no longer able to access files in the remaining packages in the connection group.</span></span>

<span data-ttu-id="92da7-126">A ordem em que o App-V procura o nome de um arquivo no grupo conexão é especificado pela ordem em que os pacotes do App-V estão listados no arquivo de manifesto do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="92da7-126">The order in which App-V looks up a file’s name in the connection group is specified by the order in which the App-V packages are listed in the connection group manifest file.</span></span>

<span data-ttu-id="92da7-127">O exemplo a seguir mostra a ordem e a relação de uma pesquisa de nome de arquivo em um grupo de conexão para **o pacote a e o** **pacote B**.</span><span class="sxs-lookup"><span data-stu-id="92da7-127">The following example shows the order and relationship of a file name lookup in a connection group for **Package A** and **Package B**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="92da7-128">Empacotar um</span><span class="sxs-lookup"><span data-stu-id="92da7-128">Package A</span></span></th>
<th align="left"><span data-ttu-id="92da7-129">Pacote B</span><span class="sxs-lookup"><span data-stu-id="92da7-129">Package B</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="92da7-130">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="92da7-130">C:\Windows\System32</span></span></p></td>
<td align="left"><p><span data-ttu-id="92da7-131">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="92da7-131">C:\Windows\System32</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="92da7-132">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="92da7-132">C:\AppTest</span></span></p></td>
<td align="left"><p><span data-ttu-id="92da7-133">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="92da7-133">C:\AppTest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="92da7-134">No exemplo acima, quando um aplicativo virtualizado tenta localizar um arquivo específico, o pacote A é pesquisado primeiro em busca de um caminho de arquivo correspondente.</span><span class="sxs-lookup"><span data-stu-id="92da7-134">In the example above, when a virtualized application tries to find a specific file, Package A is searched first for a matching file path.</span></span> <span data-ttu-id="92da7-135">Se um caminho correspondente não for encontrado, o pacote B será pesquisado usando as seguintes regras de mapeamento:</span><span class="sxs-lookup"><span data-stu-id="92da7-135">If a matching path is not found, Package B is searched, using the following mapping rules:</span></span>

-   <span data-ttu-id="92da7-136">Se um arquivo denominado **test.txt** existir na mesma hierarquia de pastas virtuais nos dois pacotes de aplicativos, o primeiro arquivo coincidente será usado.</span><span class="sxs-lookup"><span data-stu-id="92da7-136">If a file named **test.txt** exists in the same virtual folder hierarchy in both application packages, the first matching file is used.</span></span>

-   <span data-ttu-id="92da7-137">Se um arquivo chamado **bar.txt** existir na hierarquia de pastas virtuais de um pacote de aplicativo, mas não no outro, o primeiro arquivo coincidente será usado.</span><span class="sxs-lookup"><span data-stu-id="92da7-137">If a file named **bar.txt** exists in the virtual folder hierarchy of one application package, but not in the other, the first matching file is used.</span></span>






## <span data-ttu-id="92da7-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92da7-138">Related topics</span></span>


[<span data-ttu-id="92da7-139">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="92da7-139">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





