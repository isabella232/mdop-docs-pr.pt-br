---
title: Como editar Configurações GPO do MBAM 1.0
description: Como editar Configurações GPO do MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799441"
---
# <span data-ttu-id="d77c0-103">Como editar Configurações GPO do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d77c0-103">How to Edit MBAM 1.0 GPO Settings</span></span>


<span data-ttu-id="d77c0-104">Para implantar com êxito o Microsoft BitLocker Administration and Monitoring (MBAM), você deve primeiro determinar as políticas de grupo que usará na implementação da administração e do monitoramento do Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="d77c0-104">To successfully deploy Microsoft BitLocker Administration and Monitoring (MBAM), you must first determine the Group Policies that you will use in your implementation of Microsoft BitLocker Administration and Monitoring.</span></span> <span data-ttu-id="d77c0-105">Para obter mais informações sobre as várias políticas disponíveis, consulte [planejando os requisitos da política de grupo do MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d77c0-105">For more information about the various available policies, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span> <span data-ttu-id="d77c0-106">Depois de determinar as políticas que você vai usar, você deve modificar um ou mais objetos de política de grupo (GPO) que incluam as configurações de política de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d77c0-106">After you have determined the policies that you are going to use, you then must modify one or more Group Policy Objects (GPO) that include the MBAM policy settings.</span></span>

<span data-ttu-id="d77c0-107">As etapas a seguir descrevem como configurar as configurações de objeto de política de grupo (GPO) recomendadas e básicas para permitir que o MBAM gerencie a criptografia de BitLocker para os computadores cliente da sua organização.</span><span class="sxs-lookup"><span data-stu-id="d77c0-107">The following steps describe how to configure the basic, recommended Group Policy object (GPO) settings to enable MBAM to manage BitLocker encryption for your organization’s client computers.</span></span>

**<span data-ttu-id="d77c0-108">Para editar as configurações de GPO do cliente MBAM</span><span class="sxs-lookup"><span data-stu-id="d77c0-108">To edit the MBAM Client GPO settings</span></span>**

1.  <span data-ttu-id="d77c0-109">Em um computador que tenha o modelo de política de grupo do MBAM instalado, verifique se os serviços do MBAM estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="d77c0-109">On a computer that has MBAM Group Policy template installed, make sure that MBAM services are enabled.</span></span>

2.  <span data-ttu-id="d77c0-110">Use o console de gerenciamento de política de grupo (GPMC. msc) ou o produto avançado do MDOP de gerenciamento de política de grupo (AGPM) para estas ações: selecione **configuração do computador**, escolha **políticas**, clique em **modelos administrativos**, selecione **componentes do Windows**e clique em **MDOP MBAM (gerenciamento de BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="d77c0-110">Use the Group Policy Management Console (GPMC.msc) or the Advanced Group Policy Management (AGPM) MDOP product for these actions: Select **Computer configuration**, choose **Policies**, click **Administrative Templates**, select **Windows Components**, and then click **MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="d77c0-111">Edite as configurações do objeto de política de grupo necessárias para habilitar serviços de cliente do MBAM em computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="d77c0-111">Edit the Group Policy Object settings that are required to enable MBAM Client services on client computers.</span></span> <span data-ttu-id="d77c0-112">Para cada política na tabela a seguir, selecione **grupo de políticas**, clique na **política**e, em seguida, defina a **configuração**.</span><span class="sxs-lookup"><span data-stu-id="d77c0-112">For each policy in the table that follows, select **Policy Group**, click the **Policy**, and then configure the **Setting**.</span></span>

    <span data-ttu-id="d77c0-113">Grupo de políticas</span><span class="sxs-lookup"><span data-stu-id="d77c0-113">Policy Group</span></span>

    <span data-ttu-id="d77c0-114">Política</span><span class="sxs-lookup"><span data-stu-id="d77c0-114">Policy</span></span>

    <span data-ttu-id="d77c0-115">Configuração</span><span class="sxs-lookup"><span data-stu-id="d77c0-115">Setting</span></span>

    <span data-ttu-id="d77c0-116">Gerenciamento de Clientes</span><span class="sxs-lookup"><span data-stu-id="d77c0-116">Client Management</span></span>

    <span data-ttu-id="d77c0-117">Configurar os serviços do MBAM</span><span class="sxs-lookup"><span data-stu-id="d77c0-117">Configure MBAM Services</span></span>

    <span data-ttu-id="d77c0-118">Enabled.</span><span class="sxs-lookup"><span data-stu-id="d77c0-118">Enabled.</span></span> <span data-ttu-id="d77c0-119">Defina o **ponto de extremidade do serviço de hardware e recuperação do MBAM** e **Selecione informações de recuperação do BitLocker a serem armazenadas**.</span><span class="sxs-lookup"><span data-stu-id="d77c0-119">Set **MBAM Recovery and Hardware service endpoint** and **Select BitLocker recovery information to store**.</span></span>

    <span data-ttu-id="d77c0-120">Defina o **ponto de extremidade do serviço de conformidade do MBAM** e insira a **frequência do relatório de status em (minutos)**.</span><span class="sxs-lookup"><span data-stu-id="d77c0-120">Set **MBAM compliance service endpoint** and **Enter status report frequency in (minutes)**.</span></span>

    <span data-ttu-id="d77c0-121">Permitir verificação de compatibilidade de hardware</span><span class="sxs-lookup"><span data-stu-id="d77c0-121">Allow hardware compatibility checking</span></span>

    <span data-ttu-id="d77c0-122">Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d77c0-122">Disabled.</span></span> <span data-ttu-id="d77c0-123">Essa política é habilitada por padrão, mas não é necessária para uma implementação de MBAM básica.</span><span class="sxs-lookup"><span data-stu-id="d77c0-123">This policy is enabled by default, but is not needed for a basic MBAM implementation.</span></span>

    <span data-ttu-id="d77c0-124">Unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d77c0-124">Operating System Drive</span></span>

    <span data-ttu-id="d77c0-125">Configurações de criptografia de unidade do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="d77c0-125">Operating system drive encryption settings</span></span>

    <span data-ttu-id="d77c0-126">Enabled.</span><span class="sxs-lookup"><span data-stu-id="d77c0-126">Enabled.</span></span> <span data-ttu-id="d77c0-127">Defina o **protetor de seleção para unidade do sistema operacional**.</span><span class="sxs-lookup"><span data-stu-id="d77c0-127">Set **Select protector for operating system drive**.</span></span> <span data-ttu-id="d77c0-128">Isso é necessário para salvar os dados da unidade do sistema operacional no servidor de recuperação de chave MBAM.</span><span class="sxs-lookup"><span data-stu-id="d77c0-128">This is required to save operating system drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="d77c0-129">Unidade de disco removível</span><span class="sxs-lookup"><span data-stu-id="d77c0-129">Removable Drive</span></span>

    <span data-ttu-id="d77c0-130">Controlar o uso do BitLocker em unidades removíveis</span><span class="sxs-lookup"><span data-stu-id="d77c0-130">Control Use of BitLocker on removable drives</span></span>

    <span data-ttu-id="d77c0-131">Enabled.</span><span class="sxs-lookup"><span data-stu-id="d77c0-131">Enabled.</span></span> <span data-ttu-id="d77c0-132">Isso é necessário se o MBAM salvará os dados da unidade removível para o servidor de recuperação de chave do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d77c0-132">This is required if MBAM will save removable drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="d77c0-133">Unidade fixa</span><span class="sxs-lookup"><span data-stu-id="d77c0-133">Fixed Drive</span></span>

    <span data-ttu-id="d77c0-134">Controlar o uso do BitLocker em unidades fixas</span><span class="sxs-lookup"><span data-stu-id="d77c0-134">Control Use of BitLocker on fixed drives</span></span>

    <span data-ttu-id="d77c0-135">Enabled.</span><span class="sxs-lookup"><span data-stu-id="d77c0-135">Enabled.</span></span> <span data-ttu-id="d77c0-136">Isso é necessário se o MBAM salvará os dados da unidade fixa no servidor de recuperação de chave do MBAM.</span><span class="sxs-lookup"><span data-stu-id="d77c0-136">This is required if MBAM will save fixed drive data to the MBAM Key Recovery server.</span></span>

    <span data-ttu-id="d77c0-137">Definir **escolha como as unidades protegidas pelo BitLocker podem ser recuperadas** e **permitir o agente de recuperação de dados**.</span><span class="sxs-lookup"><span data-stu-id="d77c0-137">Set **Choose how BitLocker-protected drives can be recovered** and **Allow data recovery agent**.</span></span>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## <span data-ttu-id="d77c0-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d77c0-138">Related topics</span></span>


[<span data-ttu-id="d77c0-139">Implantar Objetos de Política de Grupo no MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d77c0-139">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)









