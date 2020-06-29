---
title: Planejamento da implantação do App-V 5.0 com um sistema de distribuição eletrônica de software
description: Planejamento da implantação do App-V 5.0 com um sistema de distribuição eletrônica de software
author: dansimp
ms.assetid: 8cd3f1fb-b84e-4260-9e72-a14d01e7cadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ca441820be7e6759e65902aea18b2db7f989e8f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796241"
---
# <span data-ttu-id="4a95b-103">Planejamento da implantação do App-V 5.0 com um sistema de distribuição eletrônica de software</span><span class="sxs-lookup"><span data-stu-id="4a95b-103">Planning to Deploy App-V 5.0 with an Electronic Software Distribution System</span></span>


<span data-ttu-id="4a95b-104">Se você estiver usando um sistema de distribuição de software eletrônico para implantar pacotes do App-V, examine as considerações de planejamento a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a95b-104">If you are using an electronic software distribution system to deploy App-V packages, review the following planning considerations.</span></span> <span data-ttu-id="4a95b-105">Para obter informações sobre como usar o System Center Configuration Manager para implantar o App-V, consulte [introdução ao gerenciamento de aplicativos no Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span><span class="sxs-lookup"><span data-stu-id="4a95b-105">For information about using System Center Configuration Manager to deploy App-V, see [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span></span>

<span data-ttu-id="4a95b-106">Examine as seguintes opções de componentes e requisitos de arquitetura que se aplicam quando você usa um ESD para implantar pacotes do App-V:</span><span class="sxs-lookup"><span data-stu-id="4a95b-106">Review the following component and architecture requirements options that apply when you use an ESD to deploy App-V packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4a95b-107">Requisito ou opção de implantação</span><span class="sxs-lookup"><span data-stu-id="4a95b-107">Deployment requirement or option</span></span></th>
<th align="left"><span data-ttu-id="4a95b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4a95b-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4a95b-109">O servidor de gerenciamento do App-V, o banco de dados de gerenciamento e o servidor de publicação não são necessários.</span><span class="sxs-lookup"><span data-stu-id="4a95b-109">The App-V Management server, Management database, and Publishing server are not required.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4a95b-110">Essas funções são manipuladas pela solução ESD implementada.</span><span class="sxs-lookup"><span data-stu-id="4a95b-110">These functions are handled by the implemented ESD solution.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4a95b-111">Você pode implantar o servidor de relatórios do App-V e relatar o banco de dados lado a lado com o ESD.</span><span class="sxs-lookup"><span data-stu-id="4a95b-111">You can deploy the App-V Reporting server and Reporting database side by side with the ESD.</span></span></p></td>
<td align="left"><p><span data-ttu-id="4a95b-112">A implantação lado a lado permite coletar dados e gerar relatórios.</span><span class="sxs-lookup"><span data-stu-id="4a95b-112">The side-by-side deployment lets you to collect data and generate reports.</span></span></p>
<p><span data-ttu-id="4a95b-113">Se você habilitar o cliente App-V para enviar informações de relatório e não estiver usando o servidor de relatórios do App-V, os dados de relatório serão armazenados em arquivos. xml associados.</span><span class="sxs-lookup"><span data-stu-id="4a95b-113">If you enable the App-V client to send report information, and you are not using the App-V Reporting server, the reporting data is stored in associated .xml files.</span></span></p></td>
</tr>
</tbody>
</table>

 






 

 





