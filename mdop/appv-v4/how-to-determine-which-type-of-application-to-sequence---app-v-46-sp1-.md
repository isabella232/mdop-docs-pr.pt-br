---
title: Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)
description: Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797135"
---
# <span data-ttu-id="8b9c2-103">Como determinar o tipo de aplicativo a ser sequenciado (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="8b9c2-103">How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)</span></span>


<span data-ttu-id="8b9c2-104">Você pode sequenciar três tipos básicos de aplicativos usando o Microsoft Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="8b9c2-104">You can sequence three basic types of applications by using Microsoft Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="8b9c2-105">Para determinar o tipo de aplicativo a ser sequenciado</span><span class="sxs-lookup"><span data-stu-id="8b9c2-105">To determine which type of application to sequence</span></span>


<span data-ttu-id="8b9c2-106">Use a tabela a seguir para determinar qual tipo de aplicativo você deve sequenciar e para obter mais informações sobre como sequenciar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b9c2-106">Use the following table to determine which type of application you should sequence and to obtain more information about how to sequence the application.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b9c2-107">Tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8b9c2-107">Application Type</span></span></th>
<th align="left"><span data-ttu-id="8b9c2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b9c2-108">Description</span></span></th>
<th align="left"><span data-ttu-id="8b9c2-109">Mais informações</span><span class="sxs-lookup"><span data-stu-id="8b9c2-109">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b9c2-110">Standard</span><span class="sxs-lookup"><span data-stu-id="8b9c2-110">Standard</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b9c2-111">Selecione esta opção para criar um pacote que contenha um aplicativo ou um pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8b9c2-111">Select this option to create a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="8b9c2-112">Você deve selecionar essa opção para a maioria dos aplicativos que você planeja sequenciar.</span><span class="sxs-lookup"><span data-stu-id="8b9c2-112">You should select this option for most applications that you plan to sequence.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)"><span data-ttu-id="8b9c2-113">Como sequenciar um novo aplicativo padrão (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="8b9c2-113">How to Sequence a New Standard Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b9c2-114">Complemento ou plug-in</span><span class="sxs-lookup"><span data-stu-id="8b9c2-114">Add-on or Plug-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b9c2-115">Selecione esta opção para criar um pacote que estenda a funcionalidade de um aplicativo padrão, por exemplo, um plug-in para o Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8b9c2-115">Select this option to create a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="8b9c2-116">Além disso, você pode usar plug-ins para aplicativos instalados nativamente ou outro pacote vinculado usando a composição do pacote dinâmico.</span><span class="sxs-lookup"><span data-stu-id="8b9c2-116">Additionally, you can use plug-ins for natively installed applications, or another package that is linked by using Dynamic Suite Composition.</span></span> <span data-ttu-id="8b9c2-117">Para obter mais informações sobre a composição do pacote dinâmico, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> como usar a composição do conjunto dinâmico </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="8b9c2-117">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)"><span data-ttu-id="8b9c2-118">Como sequenciar um novo complemento ou plug-in de aplicativo (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="8b9c2-118">How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b9c2-119">Middleware</span><span class="sxs-lookup"><span data-stu-id="8b9c2-119">Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b9c2-120">Selecione esta opção para criar um pacote que é necessário para um aplicativo padrão, por exemplo, o Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8b9c2-120">Select this option to create a package that is required by a standard application, for example, the Microsoft .NET Framework.</span></span> <span data-ttu-id="8b9c2-121">Os pacotes middleware são usados para a vinculação a outros pacotes usando a composição do pacote dinâmico.</span><span class="sxs-lookup"><span data-stu-id="8b9c2-121">Middleware packages are used for linking to other packages by using Dynamic Suite Composition.</span></span> <span data-ttu-id="8b9c2-122">Para obter mais informações sobre a composição do pacote dinâmico, consulte <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> como usar a composição do conjunto dinâmico </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="8b9c2-122">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)"><span data-ttu-id="8b9c2-123">Como sequenciar um novo Aplicativo middleware (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="8b9c2-123">How to Sequence a New Middleware Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8b9c2-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b9c2-124">Related topics</span></span>


[<span data-ttu-id="8b9c2-125">Tarefas do Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="8b9c2-125">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





