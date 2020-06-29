---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796785"
---
# <span data-ttu-id="f3185-103">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="f3185-103">QUERY OBJ</span></span>


<span data-ttu-id="f3185-104">Retorna uma lista delimitada por tabulação de aplicativos, pacotes, associações de tipo de arquivo ou servidores de publicação atuais.</span><span class="sxs-lookup"><span data-stu-id="f3185-104">Returns a tab-delimited list of current applications, packages, file type associations, or publishing servers.</span></span>

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f3185-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3185-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f3185-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3185-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3185-107">APPV</span><span class="sxs-lookup"><span data-stu-id="f3185-107">APP</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-108">Retorna uma lista de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f3185-108">Returns a list of applications.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3185-109">PACOTE</span><span class="sxs-lookup"><span data-stu-id="f3185-109">PACKAGE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-110">Retorna uma lista de pacotes.</span><span class="sxs-lookup"><span data-stu-id="f3185-110">Returns a list of packages.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3185-111">TYPE</span><span class="sxs-lookup"><span data-stu-id="f3185-111">TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-112">Retorna uma lista de associações de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3185-112">Returns a list of file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3185-113">SERVIDOR</span><span class="sxs-lookup"><span data-stu-id="f3185-113">SERVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-114">Retorna uma lista de servidores de publicação.</span><span class="sxs-lookup"><span data-stu-id="f3185-114">Returns a list of publishing servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3185-115">/SHORT</span><span class="sxs-lookup"><span data-stu-id="f3185-115">/SHORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-116">Sem exibir as propriedades completas de cada um, retorna uma lista de nomes de aplicativos, pacotes, associações ou nomes de servidor.</span><span class="sxs-lookup"><span data-stu-id="f3185-116">Without displaying the full properties of each, returns a list of application names, packages, associations, or server names.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3185-117">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="f3185-117">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-118">Para aplicativos, retorna todos os aplicativos conhecidos, em vez de apenas aqueles que o usuário atual tem acesso.</span><span class="sxs-lookup"><span data-stu-id="f3185-118">For applications, returns all known applications instead of only the ones the current user has access to.</span></span> <span data-ttu-id="f3185-119">Para pacotes, retorna todos os pacotes conhecidos, em vez de apenas aqueles que o usuário atual tem acesso.</span><span class="sxs-lookup"><span data-stu-id="f3185-119">For packages, returns all known packages instead of only the ones the current user has access to.</span></span> <span data-ttu-id="f3185-120">Para associações, retorna somente associações que se aplicam a todos os usuários, não àqueles específicos do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3185-120">For associations, returns only associations that apply to all users, not user-specific ones.</span></span> <span data-ttu-id="f3185-121">Não é válido para servidores.</span><span class="sxs-lookup"><span data-stu-id="f3185-121">Not valid for servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3185-122">/LOG</span><span class="sxs-lookup"><span data-stu-id="f3185-122">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-123">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="f3185-123">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f3185-124">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="f3185-124">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-125">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="f3185-125">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f3185-126">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="f3185-126">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3185-127">/LOGU</span><span class="sxs-lookup"><span data-stu-id="f3185-127">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-128">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f3185-128">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f3185-129">**Observação**  Na versão 4,6, uma nova coluna foi adicionada à saída de SFTMIME QUERY OBJ: APP \ [/GLOBAL\].</span><span class="sxs-lookup"><span data-stu-id="f3185-129">**Note** In version 4.6, a new column has been added to the output of SFTMIME QUERY OBJ:APP \[/GLOBAL\].</span></span> <span data-ttu-id="f3185-130">A última coluna da saída é um valor numérico que indica se um aplicativo foi publicado ou não.</span><span class="sxs-lookup"><span data-stu-id="f3185-130">The last column of the output is a numeric value that indicates whether an application is published or not.</span></span>

<span data-ttu-id="f3185-131">PUBLISHed = 1 significa que o aplicativo foi publicado por uma atualização do Publishing Server, instalando o aplicativo usando um arquivo do Windows Installer (. MSI) ou executando um comando adicionar pacote SFTMIME, configurar pacote ou publicar pacote usando um manifesto do pacote.</span><span class="sxs-lookup"><span data-stu-id="f3185-131">PUBLISHED=1 means the application was published by a Publishing Server refresh, by installing the application by using a Windows Installer file (.MSI), or by running an SFTMIME ADD PACKAGE, CONFIGURE PACKAGE or PUBLISH PACKAGE command by using a package manifest.</span></span>

<span data-ttu-id="f3185-132">PUBLISHed = 0 significa que o aplicativo não foi publicado ou não está mais publicado como resultado da realização de uma operação clara ou da execução de um comando de cancelamento de publicação do SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="f3185-132">PUBLISHED=0 means the application has not been published or it is no longer published as a result of performing a Clear operation or running an SFTMIME UNPUBLISH command.</span></span>

<span data-ttu-id="f3185-133">Se você usar o parâmetro/GLOBAL, o estado PUBLISHed será 1 para aplicativos que foram publicados globalmente e 0 para os aplicativos que foram publicados em contextos do usuário.</span><span class="sxs-lookup"><span data-stu-id="f3185-133">If you use the /GLOBAL parameter, the PUBLISHED state will be 1 for applications that were published globally and 0 for those applications that were published under user contexts.</span></span> <span data-ttu-id="f3185-134">Sem o parâmetro/GLOBAL, um estado publicado de 1 é retornado para aplicativos publicados no contexto do usuário que está executando o comando, e um estado de 0 é retornado para os aplicativos que são publicados globalmente.</span><span class="sxs-lookup"><span data-stu-id="f3185-134">Without the /GLOBAL parameter, a PUBLISHED state of 1 is returned for applications published in the context of the user running the command, and a state of 0 is returned for those applications that are published globally.</span></span>

 

<span data-ttu-id="f3185-135">O comando SFTMIME QUERY OBJ pode ser usado para consultar informações sobre todos os objetos mostrados acima — aplicativos, pacotes, associações de tipo de arquivo e servidores.</span><span class="sxs-lookup"><span data-stu-id="f3185-135">The SFTMIME QUERY OBJ command can be used to query for information on all of the objects shown above—applications, packages, file type associations, and servers.</span></span><span data-ttu-id="f3185-136">Para mostrar como você pode usar o comando SFTMIME QUERY OBJ em suas tarefas normais de operações, o exemplo a seguir demonstra o processo que você seguiria se quisesse definir o valor do parâmetro OVERRIDEURL para um pacote específico para especificar um novo caminho para o conteúdo do pacote.</span><span class="sxs-lookup"><span data-stu-id="f3185-136">To show how you might use the SFTMIME QUERY OBJ command in your normal operations tasks, the following example demonstrates the process you would follow if you wanted to set the OVERRIDEURL parameter value for a specific package to specify a new path to the package content.</span></span> 

1.  <span data-ttu-id="f3185-137">Para localizar o pacote que você deseja configurar, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f3185-137">To find the package that you want to configure, run the following command:</span></span>

    `SFTMIME QUERY OBJ:PACKAGE`

    <span data-ttu-id="f3185-138">Esse comando retorna cada nome de pacote descoberto como um GUID na primeira coluna de saída — por exemplo, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span><span class="sxs-lookup"><span data-stu-id="f3185-138">This command returns each discovered package name as a GUID in the first column of output—for example, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span></span>

2.  <span data-ttu-id="f3185-139">Para definir o valor do parâmetro OVERRIDEURL, use o comando [Configurar pacote](configure-package.md) do SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="f3185-139">To set the OVERRIDEURL parameter value, you use the SFTMIME [CONFIGURE PACKAGE](configure-package.md) command.</span></span> <span data-ttu-id="f3185-140">Por exemplo, para definir o valor OVERRIDEURL para esse pacote como um valor de *\\\\server\\share\\mypackage.sft*, use o comando Set Package do SFTMIME e dê a ele o GUID do pacote selecionado da saída do comando SFTMIME QUERY OBJ na etapa 1, seguido do parâmetro OVERRIDEURL e seu novo valor, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f3185-140">For example, to set the OVERRIDEURL value for this package to a value of *\\\\server\\share\\mypackage.sft*, use the SFTMIME CONFIGURE PACKAGE command and give it the selected package GUID from the output of the SFTMIME QUERY OBJ command in step 1, followed by the OVERRIDEURL parameter and its new value, as follows:</span></span>

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

<span data-ttu-id="f3185-141">Para a versão 4.6 SP2, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="f3185-141">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f3185-142">/NO-UPDATE-FTA-SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="f3185-142">/NO-UPDATE-FTA-SHORTCUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="f3185-143">Indica o estado atual do sinalizador/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="f3185-143">Indicates the current state of the /NO-UPDATE-FTA-SHORTCUT flag.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f3185-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3185-144">Related topics</span></span>


[<span data-ttu-id="f3185-145">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f3185-145">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





