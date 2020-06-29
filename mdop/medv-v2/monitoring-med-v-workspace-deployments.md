---
title: Monitoramento de implantações de espaço de trabalho da MED-V
description: Monitoramento de implantações de espaço de trabalho da MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800027"
---
# <span data-ttu-id="fec32-103">Monitoramento de implantações de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="fec32-103">Monitoring MED-V Workspace Deployments</span></span>


<span data-ttu-id="fec32-104">O recurso de monitoramento na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0 permite executar consultas em espaços de trabalho do MED-V individuais para determinar se a configuração foi bem-sucedida em toda a sua empresa após a implantação do tempo de execução dos espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="fec32-104">The monitoring feature in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 lets you run queries on individual MED-V workspaces to determine whether first time setup succeeded throughout your enterprise after the MED-V workspaces are deployed.</span></span> <span data-ttu-id="fec32-105">Monitorar o sucesso da configuração pela primeira vez é importante porque o MED-V não está em um estado utilizável até que a configuração inicial seja concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="fec32-105">Monitoring the success of first time setup is important because MED-V is not in a usable state until first time setup has been completed successfully.</span></span>

<span data-ttu-id="fec32-106">Esta seção fornece informações e instruções para ajudá-lo a monitorar o êxito ou a falha da configuração inicial.</span><span class="sxs-lookup"><span data-stu-id="fec32-106">This section provides information and instruction to assist you in monitoring the success or failure of first time setup.</span></span>

## <span data-ttu-id="fec32-107">Para monitorar implantações de espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="fec32-107">To monitor MED-V workspace deployments</span></span>


<span data-ttu-id="fec32-108">O recurso de monitoramento consiste em um provedor de instrumentação de gerenciamento do Windows (WMI) que você pode consultar usando a linguagem de consulta WMI para descobrir o status da primeira configuração para todos os usuários finais em um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="fec32-108">The monitoring feature consists of a coupled in-process Windows Management Instrumentation (WMI) provider that you can query using WMI Query Language to discover the status of first time setup for all end users on a MED-V workspace.</span></span>

<span data-ttu-id="fec32-109">O provedor WMI é implementado usando a estrutura de extensão do provedor WMI do Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="fec32-109">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span> <span data-ttu-id="fec32-110">O provedor WMI é executado no contexto de LocalService e armazena na primeira vez que o estado da configuração é seguro em \\ProgramData.</span><span class="sxs-lookup"><span data-stu-id="fec32-110">The WMI provider executes in the context of LocalService and stores the first time setup state securely under \\ProgramData.</span></span>

<span data-ttu-id="fec32-111">O provedor WMI é implementado no namespace **root\\microsoft\\medv** e implementa a classe **FTS \ _Status**, que expõe o método **SetFtsState**.</span><span class="sxs-lookup"><span data-stu-id="fec32-111">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **FTS\_Status**, which exposes the method **SetFtsState**.</span></span> <span data-ttu-id="fec32-112">O MED-V usa **SetFtsState** para definir o estado de configuração da primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fec32-112">MED-V uses **SetFtsState** to set the first time setup state.</span></span>

<span data-ttu-id="fec32-113">A classe contém as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="fec32-113">The class contains the following properties.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fec32-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fec32-114">Property</span></span></th>
<th align="left"><span data-ttu-id="fec32-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="fec32-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fec32-116">Computador</span><span class="sxs-lookup"><span data-stu-id="fec32-116">Machine</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fec32-117">Propriedade somente leitura </strong> que contém o nome da máquina virtual convidada provisionada pela primeira configuração de tempo.</span><span class="sxs-lookup"><span data-stu-id="fec32-117">Read Only</strong> property that contains the name of the guest virtual machine provisioned by first time setup.</span></span> <span data-ttu-id="fec32-118">Esta chave contém o nome que o convidado teria na primeira falha na configuração da primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fec32-118">This key contains the name that the guest would have had on first time setup failure.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fec32-119">StatusCode</span><span class="sxs-lookup"><span data-stu-id="fec32-119">StatusCode</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="fec32-120">Propriedade somente leitura </strong> que contém zero se a configuração da primeira vez for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fec32-120">Read Only</strong> property that contains zero if first time setup succeeded.</span></span> <span data-ttu-id="fec32-121">Qualquer outro valor retornado será igual à identificação do evento que é registrado.</span><span class="sxs-lookup"><span data-stu-id="fec32-121">Any other value returned equals the event ID for the error that is logged.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fec32-122">Hora</span><span class="sxs-lookup"><span data-stu-id="fec32-122">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fec32-123">A hora UTC em que a configuração da primeira vez foi concluída.</span><span class="sxs-lookup"><span data-stu-id="fec32-123">The UTC time that first time setup completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fec32-124">Usuário</span><span class="sxs-lookup"><span data-stu-id="fec32-124">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fec32-125">O usuário pela primeira vez em que a configuração foi executada.</span><span class="sxs-lookup"><span data-stu-id="fec32-125">The user for which first time setup was run.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fec32-126">O código a seguir mostra o arquivo MOF (formato de objeto gerenciado) que define a classe **FTS \ _Status** .</span><span class="sxs-lookup"><span data-stu-id="fec32-126">The following code shows the Managed Object Format (MOF) file that defines the **FTS\_Status** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

<span data-ttu-id="fec32-127">Como sua principal preocupação é mais provável que os espaços de trabalho do MED-V para os quais a configuração da primeira configuração não foram concluídas com êxito, você pode gravar sua consulta para retornar apenas aquelas que falharam na configuração inicial, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fec32-127">Because your main concern is most likely those MED-V workspaces for which first time setup was not completed successfully, you can write your query to only return those that failed first time setup, for example:</span></span>

``` syntax
Select * from FTS_Status where StatusCode != 0
```

<span data-ttu-id="fec32-128">Nesse caso, o recurso de monitoramento retorna uma lista dos espaços de trabalho do MED-V que falharam durante a configuração inicial, que você pode usar para realizar as ações adequadas para resolver a falha.</span><span class="sxs-lookup"><span data-stu-id="fec32-128">In this case, the monitoring feature returns a list of those MED-V workspaces that failed first time setup, which you can use to take the appropriate actions to resolve the failure.</span></span>

## <span data-ttu-id="fec32-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fec32-129">Related topics</span></span>


[<span data-ttu-id="fec32-130">Monitorar espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="fec32-130">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="fec32-131">Como verificar as configurações da primeira instalação</span><span class="sxs-lookup"><span data-stu-id="fec32-131">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

 

 





