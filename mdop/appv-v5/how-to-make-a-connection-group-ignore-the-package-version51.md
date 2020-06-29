---
title: Como criar um grupo de conexão para ignorar a versão do pacote
description: Como criar um grupo de conexão para ignorar a versão do pacote
author: dansimp
ms.assetid: db16b095-dbe2-42c7-863d-b0d5d91b2f4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 026ef1b3a2aa073a684b1fe5da4f79aa1067072d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796373"
---
# <span data-ttu-id="44932-103">Como criar um grupo de conexão para ignorar a versão do pacote</span><span class="sxs-lookup"><span data-stu-id="44932-103">How to Make a Connection Group Ignore the Package Version</span></span>


<span data-ttu-id="44932-104">O 5,1 do Microsoft Application Virtualization (App-V) permite que você configure um grupo de conexão para usar qualquer versão de um pacote, que simplifica as atualizações do pacote e reduz o número de grupos de conexão que você precisa criar.</span><span class="sxs-lookup"><span data-stu-id="44932-104">Microsoft Application Virtualization (App-V) 5.1 lets you configure a connection group to use any version of a package, which simplifies package upgrades and reduces the number of connection groups you need to create.</span></span>

<span data-ttu-id="44932-105">Para atualizar um pacote em algumas versões anteriores do App-V, você precisava executar várias etapas, incluindo a desabilitação do grupo de conexão e a modificação do arquivo de definição XML do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="44932-105">To upgrade a package in some earlier versions of App-V, you had to perform several steps, including disabling the connection group and modifying the connection group’s XML definition file.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44932-106">Descrição da tarefa com o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="44932-106">Task description with App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="44932-107">Como executar a tarefa com o App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="44932-107">How to perform the task with App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44932-108">Você pode configurar um grupo de conexão para aceitar qualquer versão de um pacote, o que permite que você atualize o pacote sem precisar desabilitar o grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="44932-108">You can configure a connection group to accept any version of a package, which enables you to upgrade the package without having to disable the connection group.</span></span></p>
<p><strong><span data-ttu-id="44932-109">Como funciona o recurso:</span><span class="sxs-lookup"><span data-stu-id="44932-109">How the feature works:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="44932-110">Se o grupo de conexão tiver acesso a várias versões de um pacote, a versão mais recente será usada.</span><span class="sxs-lookup"><span data-stu-id="44932-110">If the connection group has access to multiple versions of a package, the latest version is used.</span></span></p></li>
<li><p><span data-ttu-id="44932-111">Se o grupo de conexão contiver um pacote opcional com uma versão incorreta, o pacote será ignorado e não bloqueará a criação do ambiente virtual do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="44932-111">If the connection group contains an optional package that has an incorrect version, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></li>
<li><p><span data-ttu-id="44932-112">Se o grupo de conexão contém um pacote não opcional com uma versão incorreta, o ambiente virtual do grupo de conexão não pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="44932-112">If the connection group contains a non-optional package that has an incorrect version, the connection group’s virtual environment cannot be created.</span></span></p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="44932-113">Método</span><span class="sxs-lookup"><span data-stu-id="44932-113">Method</span></span></th>
<th align="left"><span data-ttu-id="44932-114">Etapas</span><span class="sxs-lookup"><span data-stu-id="44932-114">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="44932-115">Servidor App-V – console de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="44932-115">App-V Server – Management Console</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="44932-116">No console de gerenciamento, selecione <strong> grupos de conexão </strong> .</span><span class="sxs-lookup"><span data-stu-id="44932-116">In the Management Console, select <strong>CONNECTION GROUPS</strong>.</span></span></p></li>
<li><p><span data-ttu-id="44932-117">Selecione o grupo de conexões correto da biblioteca de grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="44932-117">Select the correct connection group from the Connection Groups library.</span></span></p></li>
<li><p><span data-ttu-id="44932-118">Clique em <strong> Editar </strong> no painel pacotes conectados.</span><span class="sxs-lookup"><span data-stu-id="44932-118">Click <strong>EDIT</strong> in the CONNECTED PACKAGES pane.</span></span></p></li>
<li><p><span data-ttu-id="44932-119">Marque <strong> </strong> a caixa de seleção usar qualquer versão ao lado do nome do pacote e clique em <strong> aplicar </strong> .</span><span class="sxs-lookup"><span data-stu-id="44932-119">Select <strong>Use Any Version</strong> check box next to the package name, and click <strong>Apply</strong>.</span></span></p></li>
</ol>
<p><span data-ttu-id="44932-120">Para saber mais sobre como adicionar ou atualizar pacotes, consulte <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)"> como adicionar ou atualizar pacotes usando o console de gerenciamento </a> .</span><span class="sxs-lookup"><span data-stu-id="44932-120">For more about adding or upgrading packages, see <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)">How to Add or Upgrade Packages by Using the Management Console</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="44932-121">Cliente App-V em um computador autônomo</span><span class="sxs-lookup"><span data-stu-id="44932-121">App-V Client on a Stand-alone computer</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="44932-122">Crie o documento XML do grupo de conexão.</span><span class="sxs-lookup"><span data-stu-id="44932-122">Create the connection group XML document.</span></span></p></li>
<li><p><span data-ttu-id="44932-123">Para que o pacote seja atualizado, defina o <strong> atributo de marca do pacote </strong> <strong> VersionId </strong> como um asterisco ( <strong>\*</strong> ).</span><span class="sxs-lookup"><span data-stu-id="44932-123">For the package to be upgraded, set the <strong>Package</strong> tag attribute <strong>VersionID</strong> to an asterisk (<strong>\*</strong>).</span></span></p></li>
<li><p><span data-ttu-id="44932-124">Use o cmdlet a seguir para adicionar o grupo de conexão e incluir o caminho para o documento XML do grupo de conexões:</span><span class="sxs-lookup"><span data-stu-id="44932-124">Use the following cmdlet to add the connection group, and include the path to the connection group XML document:</span></span></p>
<p><strong><span data-ttu-id="44932-125">Add-AppvClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="44932-125">Add-AppvClientConnectionGroup</span></span></strong></p></li>
<li><p><span data-ttu-id="44932-126">Ao atualizar um pacote, use os seguintes cmdlets para remover o pacote antigo, adicionar o pacote atualizado e publicar o pacote atualizado:</span><span class="sxs-lookup"><span data-stu-id="44932-126">When you upgrade a package, use the following cmdlets to remove the old package, add the upgraded package, and publish the upgraded package:</span></span></p>
<ul>
<li><p><span data-ttu-id="44932-127">RemoveAppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="44932-127">RemoveAppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="44932-128">Add-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="44932-128">Add-AppvClientPackage</span></span></p></li>
<li><p><span data-ttu-id="44932-129">Publicar-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="44932-129">Publish-AppvClientPackage</span></span></p></li>
</ul></li>
</ol>
<p><span data-ttu-id="44932-130">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="44932-130">For more information, see:</span></span></p>
<ul>
<li><p><span data-ttu-id="44932-131">O arquivo XML de exemplo, o <strong> arquivo XML do grupo de conexão com pacotes opcionais </strong> , nesta seção: <a href="how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional)"> como usar pacotes opcionais em grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="44932-131">The example XML file, <strong>Connection group XML file with optional packages</strong>, in this section: <a href="how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md#bkmk-apps-plugs-optional)">How to Use Optional Packages in Connection Groups</span></span></a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"><span data-ttu-id="44932-132">Como gerenciar pacotes do App-V 5.1 em execução em um computador autônomo usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="44932-132">How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="44932-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44932-133">Related topics</span></span>


[<span data-ttu-id="44932-134">Gerenciando grupos de conexão</span><span class="sxs-lookup"><span data-stu-id="44932-134">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





