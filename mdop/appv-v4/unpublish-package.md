---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796664"
---
# <span data-ttu-id="db973-103">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="db973-103">UNPUBLISH PACKAGE</span></span>


<span data-ttu-id="db973-104">Permite remover os atalhos e tipos de arquivo para um pacote inteiro.</span><span class="sxs-lookup"><span data-stu-id="db973-104">Enables you to remove the shortcuts and file types for an entire package.</span></span>

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db973-105">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="db973-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="db973-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="db973-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db973-107">PACKAGE: &lt; Package-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="db973-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="db973-108">O nome do pacote.</span><span class="sxs-lookup"><span data-stu-id="db973-108">The name of the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db973-109">/CLEAR</span><span class="sxs-lookup"><span data-stu-id="db973-109">/CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="db973-110">Se houver, as configurações do usuário também serão removidas.</span><span class="sxs-lookup"><span data-stu-id="db973-110">If present, user settings will also be removed.</span></span> <span data-ttu-id="db973-111">(Para obter mais informações, consulte a observação importante posteriormente neste tópico.)</span><span class="sxs-lookup"><span data-stu-id="db973-111">(For more information, see the Important note later in this topic.)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db973-112">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="db973-112">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="db973-113">Se estiver presente, o pacote será cancelado para todos os usuários neste computador.</span><span class="sxs-lookup"><span data-stu-id="db973-113">If present, the package will be unpublished for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db973-114">/LOG</span><span class="sxs-lookup"><span data-stu-id="db973-114">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="db973-115">Se especificado, a saída será registrada no nome do caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="db973-115">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db973-116">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="db973-116">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="db973-117">Se especificado, a saída será apresentada na janela ativa do console (padrão).</span><span class="sxs-lookup"><span data-stu-id="db973-117">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db973-118">/GUI</span><span class="sxs-lookup"><span data-stu-id="db973-118">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="db973-119">Se especificado, a saída será apresentada em uma caixa de diálogo do Windows.</span><span class="sxs-lookup"><span data-stu-id="db973-119">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="db973-120">Para a versão 4.6, a seguinte opção foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="db973-120">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db973-121">/LOGU</span><span class="sxs-lookup"><span data-stu-id="db973-121">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="db973-122">Se especificado, a saída será registrada no nome do caminho especificado no formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="db973-122">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="db973-123">**Importante**  Antes de poder executar o comando **Cancelar publicação do pacote** , o pacote já deve ter sido adicionado ao cliente do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="db973-123">**Important** Before you can run the **UNPUBLISH PACKAGE** command, the package must already have been added to the Application Virtualization Client.</span></span>

<span data-ttu-id="db973-124">Para usar o pacote **global**de **cancelamento de publicação** deve ser executado como administrador local; caso contrário, somente a permissão **ClearApp** é necessária.</span><span class="sxs-lookup"><span data-stu-id="db973-124">To use **GLOBAL**, **UNPUBLISH PACKAGE** must be run as local Administrator; otherwise, only **ClearApp** permission is needed.</span></span>

<span data-ttu-id="db973-125">Usar o **pacote não publicar** com **global** remove todos os tipos de arquivo e atalhos globais do pacote.</span><span class="sxs-lookup"><span data-stu-id="db973-125">Using **UNPUBLISH PACKAGE** with **GLOBAL** removes any global file types and shortcuts for the package.</span></span> <span data-ttu-id="db973-126">**Clear** não é aplicável.</span><span class="sxs-lookup"><span data-stu-id="db973-126">**CLEAR** is not applicable.</span></span>

<span data-ttu-id="db973-127">Usar o **pacote não publicar** sem a **global** remove os atalhos de usuário e os tipos de arquivo do pacote e, se **limpar** estiver definido, também removerá as configurações do usuário e interromperá as cargas em segundo plano sob o contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="db973-127">Using **UNPUBLISH PACKAGE** without **GLOBAL** removes the user shortcuts and file types for the package and, if **CLEAR** is set, also removes user settings and stops background loads under the user’s context.</span></span>

<span data-ttu-id="db973-128">O **CANcelamento de publicação do pacote** funciona em aplicativos do mesmo nome ou GUID do pacote que foi usado como a ID da fonte para **Adicionar**, **Editar**e **publicar pacote**.</span><span class="sxs-lookup"><span data-stu-id="db973-128">**UNPUBLISH PACKAGE** works on applications from the same package name or GUID that was used as the source ID for **ADD**, **EDIT**, and **PUBLISH PACKAGE**.</span></span>

<span data-ttu-id="db973-129">A opção **Cancelar publicação do pacote** sempre limpa todas as configurações do usuário, atalhos e tipos de arquivo, independentemente do uso da opção/Clear</span><span class="sxs-lookup"><span data-stu-id="db973-129">**UNPUBLISH PACKAGE** always clears all the user settings, shortcuts, and file types regardless of the use of the /CLEAR switch.</span></span>

 

## <span data-ttu-id="db973-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db973-130">Related topics</span></span>


[<span data-ttu-id="db973-131">Referência de comando SFTMIME</span><span class="sxs-lookup"><span data-stu-id="db973-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





