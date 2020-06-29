---
title: Editando as configurações de Política de Grupo do MBAM 2.5
description: Editando as configurações de Política de Grupo do MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796039"
---
# <span data-ttu-id="4a3df-103">Editando as configurações de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4a3df-103">Editing the MBAM 2.5 Group Policy Settings</span></span>


<span data-ttu-id="4a3df-104">Para implantar com êxito o Microsoft BitLocker Administration and Monitoring (MBAM), você precisa:</span><span class="sxs-lookup"><span data-stu-id="4a3df-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4a3df-105">Tarefa</span><span class="sxs-lookup"><span data-stu-id="4a3df-105">Task</span></span></th>
<th align="left"><span data-ttu-id="4a3df-106">Mais informações</span><span class="sxs-lookup"><span data-stu-id="4a3df-106">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4a3df-107">Copie os modelos de política de grupo do MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="4a3df-107">Copy the MBAM 2.5 Group Policy Templates.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="4a3df-108">Copiando os modelos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4a3df-108">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4a3df-109">Determine quais objetos de política de grupo (GPOs) você deseja usar na implementação do MBAM.</span><span class="sxs-lookup"><span data-stu-id="4a3df-109">Determine which Group Policy Objects (GPOs) you want to use in your MBAM implementation.</span></span> <span data-ttu-id="4a3df-110">Com base nas necessidades da sua organização, talvez seja necessário definir configurações adicionais de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="4a3df-110">Based on the needs of your organization, you might have to configure additional Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)"><span data-ttu-id="4a3df-111">Planejando os requisitos da política de grupo do MBAM 2,5 </a> – contém descrições dos GPOs</span><span class="sxs-lookup"><span data-stu-id="4a3df-111">Planning for MBAM 2.5 Group Policy Requirements</a> – contains descriptions of the GPOs</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4a3df-112">Defina as configurações de política de grupo da sua organização.</span><span class="sxs-lookup"><span data-stu-id="4a3df-112">Set the Group Policy settings for your organization.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4a3df-113">**Importante**  Não altere as configurações de política de grupo no nó de **criptografia de unidade de disco BitLocker** , ou o MBAM não funcionará corretamente.</span><span class="sxs-lookup"><span data-stu-id="4a3df-113">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node, or MBAM will not work correctly.</span></span> <span data-ttu-id="4a3df-114">Ao definir as configurações de política de grupo no nó **MDOP MBAM (gerenciamento de BitLocker)** , o MBAM configura automaticamente as configurações de **criptografia de unidade de disco BitLocker** para você.</span><span class="sxs-lookup"><span data-stu-id="4a3df-114">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="4a3df-115">Para editar configurações de política de grupo do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="4a3df-115">To edit MBAM Client Group Policy settings</span></span>**

1.  <span data-ttu-id="4a3df-116">Em um computador que tenha os modelos de política de grupo do MBAM instalados, verifique se os serviços do MBAM estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="4a3df-116">On a computer that has the MBAM Group Policy Templates installed, make sure that MBAM Services are enabled.</span></span>

2.  <span data-ttu-id="4a3df-117">Usando o console de gerenciamento de política de grupo (GPMC. msc) ou o produto do MDOP gerenciamento de política de grupo avançado da Microsoft em um computador com os modelos de política de grupo do MBAM instalados, selecione políticas de **configuração do computador** &gt; **Policies** &gt; **modelos** &gt; **Windows Components** &gt; **do Windows MDOP MBAM (gerenciamento de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="4a3df-117">Using the Group Policy Management Console (GPMC.msc) or the Microsoft Advanced Group Policy Management MDOP product on a computer with the MBAM Group Policy Templates installed, select **Computer configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="4a3df-118">Edite as configurações de política de grupo necessárias para habilitar serviços de cliente do MBAM em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="4a3df-118">Edit the Group Policy settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="4a3df-119">Para cada política na tabela a seguir, selecione **grupo de políticas**, clique na **política** desejada e, em seguida, defina as configurações.</span><span class="sxs-lookup"><span data-stu-id="4a3df-119">For each policy in the following table, select **Policy Group**, click the **Policy** you want, and then configure the settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="4a3df-120">Grupo de políticas</span><span class="sxs-lookup"><span data-stu-id="4a3df-120">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="4a3df-121">Política</span><span class="sxs-lookup"><span data-stu-id="4a3df-121">Policy</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4a3df-122">Gerenciamento de Clientes</span><span class="sxs-lookup"><span data-stu-id="4a3df-122">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4a3df-123">Configurar os serviços do MBAM</span><span class="sxs-lookup"><span data-stu-id="4a3df-123">Configure MBAM Services</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4a3df-124">Unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4a3df-124">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4a3df-125">Configurações de criptografia de unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="4a3df-125">Operating system drive encryption settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4a3df-126">Unidade de disco removível</span><span class="sxs-lookup"><span data-stu-id="4a3df-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4a3df-127">Controlar o uso do BitLocker em unidades removíveis</span><span class="sxs-lookup"><span data-stu-id="4a3df-127">Control use of BitLocker on removable drives</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="4a3df-128">Unidade fixa</span><span class="sxs-lookup"><span data-stu-id="4a3df-128">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4a3df-129">Controlar o uso do BitLocker em unidades fixas</span><span class="sxs-lookup"><span data-stu-id="4a3df-129">Control use of BitLocker on fixed drives</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="4a3df-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a3df-130">Related topics</span></span>


[<span data-ttu-id="4a3df-131">Planejamento para os requisitos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4a3df-131">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)

[<span data-ttu-id="4a3df-132">Copiando os modelos de Política de Grupo do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4a3df-132">Copying the MBAM 2.5 Group Policy Templates</span></span>](copying-the-mbam-25-group-policy-templates.md)

 
## <span data-ttu-id="4a3df-133">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="4a3df-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4a3df-134">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4a3df-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4a3df-135">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4a3df-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





