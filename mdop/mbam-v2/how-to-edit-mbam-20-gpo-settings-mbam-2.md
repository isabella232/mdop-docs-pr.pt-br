---
title: Como editar Configurações GPO do MBAM 2.0
description: Como editar Configurações GPO do MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799402"
---
# <span data-ttu-id="836ee-103">Como editar Configurações GPO do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="836ee-103">How to Edit MBAM 2.0 GPO Settings</span></span>


<span data-ttu-id="836ee-104">Para implantar com êxito o Microsoft BitLocker Administration and Monitoring (MBAM), primeiro você precisa determinar as políticas de grupo que usará na implementação da administração e do monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="836ee-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you first have to determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="836ee-105">Consulte [planejando os requisitos da política de grupo do MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) para obter mais informações sobre as diferentes políticas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="836ee-105">See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for more information on the different policies that are available.</span></span> <span data-ttu-id="836ee-106">Depois de determinar as políticas que você vai usar, você deve modificar um ou mais objetos de política de grupo (GPO) que incluam as configurações de política para MBAM.</span><span class="sxs-lookup"><span data-stu-id="836ee-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the policy settings for MBAM.</span></span>

<span data-ttu-id="836ee-107">Você pode usar as etapas a seguir para configurar as configurações básicas e recomendadas do GPO para permitir que o MBAM gerencie a criptografia de BitLocker para os computadores cliente da sua organização.</span><span class="sxs-lookup"><span data-stu-id="836ee-107">You can use the following steps to configure the basic, recommended GPO settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="836ee-108">Para editar as configurações de GPO do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="836ee-108">To Edit MBAM Client GPO Settings</span></span>**

1.  <span data-ttu-id="836ee-109">Em um computador que tenha o modelo de política de grupo do MBAM instalado, verifique se os serviços do MBAM estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="836ee-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="836ee-110">Usando o console de gerenciamento de política de grupo (GPMC. msc) ou o produto avançado do MDOP do gerenciamento de política de grupo (AGPM) em um computador com o modelo de política de grupo do MBAM instalado, selecione **configuração do computador**, escolha **políticas**, clique em **modelos administrativos**, selecione **componentes do Windows**e clique em **MDOP MBAM (gerenciamento de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="836ee-110">Using the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product on a computer with the MBAM Group Policy template installed, select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="836ee-111">Edite as configurações do objeto de política de grupo necessárias para habilitar serviços de cliente do MBAM em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="836ee-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="836ee-112">Para cada política na tabela a seguir, selecione **grupo de políticas**, clique na **política**e, em seguida, defina a **configuração**:</span><span class="sxs-lookup"><span data-stu-id="836ee-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="836ee-113">Grupo de políticas</span><span class="sxs-lookup"><span data-stu-id="836ee-113">Policy Group</span></span></th>
    <th align="left"><span data-ttu-id="836ee-114">Política</span><span class="sxs-lookup"><span data-stu-id="836ee-114">Policy</span></span></th>
    <th align="left"><span data-ttu-id="836ee-115">Configuração</span><span class="sxs-lookup"><span data-stu-id="836ee-115">Setting</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="836ee-116">Gerenciamento de Clientes</span><span class="sxs-lookup"><span data-stu-id="836ee-116">Client Management</span></span></p></td>
    <td align="left"><p><span data-ttu-id="836ee-117">Configurar os serviços do MBAM</span><span class="sxs-lookup"><span data-stu-id="836ee-117">Configure MBAM Services</span></span></p></td>
    <td align="left"><p><span data-ttu-id="836ee-118">Enabled.</span><span class="sxs-lookup"><span data-stu-id="836ee-118">Enabled.</span></span> <span data-ttu-id="836ee-119">Defina o <strong> ponto de extremidade do serviço de hardware e recuperação do MBAM </strong> e <strong> Selecione informações de recuperação do BitLocker a serem armazenadas </strong> .</span><span class="sxs-lookup"><span data-stu-id="836ee-119">Set <strong>MBAM Recovery and Hardware service endpoint</strong> and <strong>Select BitLocker recovery information to store</strong>.</span></span> <span data-ttu-id="836ee-120">Defina o <strong> ponto de extremidade do serviço de conformidade </strong> do MBAM e insira a frequência do relatório de status em (minutos).</span><span class="sxs-lookup"><span data-stu-id="836ee-120">Set <strong>MBAM compliance service endpoint</strong> and Enter status report frequency in (minutes).</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="836ee-121">Unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="836ee-121">Operating System Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="836ee-122">Configurações de criptografia de unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="836ee-122">Operating system drive encryption settings</span></span></p></td>
    <td align="left"><p><span data-ttu-id="836ee-123">Enabled.</span><span class="sxs-lookup"><span data-stu-id="836ee-123">Enabled.</span></span> <span data-ttu-id="836ee-124">Defina o <strong> protetor de seleção para unidade do sistema operacional </strong> .</span><span class="sxs-lookup"><span data-stu-id="836ee-124">Set <strong>Select protector for operating system drive</strong>.</span></span> <span data-ttu-id="836ee-125">É necessário para salvar os dados da unidade do sistema operacional no servidor de recuperação do MBAMKey.</span><span class="sxs-lookup"><span data-stu-id="836ee-125">Required to save operating system drive data to the MBAMKey Recovery server.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="836ee-126">Unidade de disco removível</span><span class="sxs-lookup"><span data-stu-id="836ee-126">Removable Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="836ee-127">Controlar o uso do BitLocker em unidades removíveis</span><span class="sxs-lookup"><span data-stu-id="836ee-127">Control Use of BitLocker on removable drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="836ee-128">Enabled.</span><span class="sxs-lookup"><span data-stu-id="836ee-128">Enabled.</span></span> <span data-ttu-id="836ee-129">Obrigatório se o MBAM salvar os dados da unidade removível para o servidor de recuperação de chave do MBAM.</span><span class="sxs-lookup"><span data-stu-id="836ee-129">Required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="836ee-130">Unidade fixa</span><span class="sxs-lookup"><span data-stu-id="836ee-130">Fixed Drive</span></span></p></td>
    <td align="left"><p><span data-ttu-id="836ee-131">Controlar o uso do BitLocker em unidades fixas</span><span class="sxs-lookup"><span data-stu-id="836ee-131">Control Use of BitLocker on fixed drives</span></span></p></td>
    <td align="left"><p><span data-ttu-id="836ee-132">Enabled.</span><span class="sxs-lookup"><span data-stu-id="836ee-132">Enabled.</span></span> <span data-ttu-id="836ee-133">Obrigatório se o MBAM salvará os dados da unidade fixa no servidor de recuperação de chave do MBAM.</span><span class="sxs-lookup"><span data-stu-id="836ee-133">Required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span></p>
    <p><span data-ttu-id="836ee-134">Definir <strong> escolha como as unidades protegidas pelo BitLocker podem ser recuperadas </strong> e <strong> permitir o agente de recuperação de dados </strong> .</span><span class="sxs-lookup"><span data-stu-id="836ee-134">Set <strong>Choose how BitLocker-protected drives can be recovered</strong> and <strong>Allow data recovery agent</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="836ee-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="836ee-135">Related topics</span></span>


[<span data-ttu-id="836ee-136">Implantar Objetos de Política de Grupo no MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="836ee-136">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)









