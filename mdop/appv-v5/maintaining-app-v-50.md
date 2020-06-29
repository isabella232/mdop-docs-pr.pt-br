---
title: Manutenção do App-V 5.0
description: Manutenção do App-V 5.0
author: dansimp
ms.assetid: 66851ec3-c674-493b-ad6d-db8fcbf1956c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3445bfe00ba7703a66fa3da2f9d7089990dd3854
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796294"
---
# <span data-ttu-id="999a3-103">Manutenção do App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="999a3-103">Maintaining App-V 5.0</span></span>


<span data-ttu-id="999a3-104">Depois de concluir todos os planejamentos necessários e, em seguida, a implantação do App-V 5,0, você pode usar as seguintes informações para manter a infraestrutura do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="999a3-104">After you have completed all the necessary planning, and then deployment of App-V 5.0, you can use the following information to maintain the App-V 5.0 infrastructure.</span></span>

## <a href="" id="move-the-app-v-5-0-server-"></a><span data-ttu-id="999a3-105">Mover o servidor do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="999a3-105">Move the App-V 5.0 Server</span></span>


<span data-ttu-id="999a3-106">O servidor do App-V 5,0 se conecta ao banco de dados do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="999a3-106">The App-V 5.0 server connects to the App-V 5.0 database.</span></span> <span data-ttu-id="999a3-107">Portanto, você pode instalar o componente de gerenciamento em qualquer computador na rede e, em seguida, conectá-lo ao banco de dados do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="999a3-107">Therefore you can install the management component to any computer on the network and then connect it to the App-V 5.0 database.</span></span>

[<span data-ttu-id="999a3-108">Como mover o servidor do App-V para outro computador</span><span class="sxs-lookup"><span data-stu-id="999a3-108">How to Move the App-V Server to Another Computer</span></span>](how-to-move-the-app-v-server-to-another-computer.md)

## <a href="" id="determine-if-an-app-v-5-0-application-is-running-virtualized-"></a><span data-ttu-id="999a3-109">Determinar se um aplicativo App-V 5,0 está em execução virtualizado</span><span class="sxs-lookup"><span data-stu-id="999a3-109">Determine if an App-V 5.0 Application is Running Virtualized</span></span>


<span data-ttu-id="999a3-110">ISVs (fornecedores independentes de software) que desejam determinar se um aplicativo está em execução virtualizada com o App-V 5,0 ou superior, deve abrir um objeto nomeado chamado \*\*AppVVirtual- &lt; pid &gt; \*\* no namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="999a3-110">Independent software vendors (ISV) who want to determine if an application is running virtualized with App-V 5.0 or above, should open a named object called **AppVVirtual-&lt;PID&gt;** in the default namespace.</span></span> <span data-ttu-id="999a3-111">Por exemplo, a API do Windows **GetCurrentProcessId ()** pode ser usada para obter a ID do processo atual, por exemplo, 4052, e, em seguida, se um objeto de evento nomeado chamado **AppVVirtual-4052** puder ser aberto com êxito usando **OpenEvent ()** no namespace padrão para acesso de leitura, o aplicativo será virtual.</span><span class="sxs-lookup"><span data-stu-id="999a3-111">For example, Windows API **GetCurrentProcessId()** can be used to obtain the current process's ID, for example 4052, and then if a named Event object called **AppVVirtual-4052** can be successfully opened using **OpenEvent()** in the default namespace for read access, then the application is virtual.</span></span> <span data-ttu-id="999a3-112">Se a chamada **OpenEvent ()** falhar, o aplicativo não será virtual.</span><span class="sxs-lookup"><span data-stu-id="999a3-112">If the **OpenEvent()** call fails, the application is not virtual.</span></span>

<span data-ttu-id="999a3-113">Além disso, os ISVs que desejam virtualizar ou não virtualizam explicitamente chamadas em APIs específicas com o App-V 5,0 e superior podem usar as funções **VirtualizeCurrentThread ()** e **CurrentThreadIsVirtualized ()** implementadas no módulo AppEntSubsystems32.dll.</span><span class="sxs-lookup"><span data-stu-id="999a3-113">Additionally, ISV’s who want to explicitly virtualize or not virtualize calls on specific API’s with App-V 5.0 and above, can use the **VirtualizeCurrentThread()** and **CurrentThreadIsVirtualized()** functions implemented in the AppEntSubsystems32.dll module.</span></span> <span data-ttu-id="999a3-114">Elas fornecem uma maneira de fazer uma referência a um componente downstream em que a chamada deve ou não ser virtualizada.</span><span class="sxs-lookup"><span data-stu-id="999a3-114">These provide a way of hinting at a downstream component that the call should or should not be virtualized.</span></span>






## <span data-ttu-id="999a3-115">Outros recursos para manter o App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="999a3-115">Other resources for maintaining App-V 5.0</span></span>


[<span data-ttu-id="999a3-116">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="999a3-116">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





