---
title: Planejamento para a migração de uma versão anterior do App-V
description: Planejamento para a migração de uma versão anterior do App-V
author: dansimp
ms.assetid: d4ca8f09-86fd-456f-8ec2-242ff94ae9a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2242f58a29473e116506ec013b94a79d1bb814a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796258"
---
# <span data-ttu-id="1dc31-103">Planejamento para a migração de uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="1dc31-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="1dc31-104">Use as informações a seguir para planejar como migrar para o App-V 5,0 de versões anteriores do App-V.</span><span class="sxs-lookup"><span data-stu-id="1dc31-104">Use the following information to plan how to migrate to App-V 5.0 from previous versions of App-V.</span></span>

## <span data-ttu-id="1dc31-105">Requisitos de migração</span><span class="sxs-lookup"><span data-stu-id="1dc31-105">Migration requirements</span></span>


<span data-ttu-id="1dc31-106">Antes de iniciar qualquer atualização, examine os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="1dc31-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="1dc31-107">Se você estiver atualizando de uma versão anterior ao App-V 4,6 SP2, atualize para a versão App-V 4,6 SP3 primeiro antes de atualizar para o App-V 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1dc31-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.0 or later.</span></span> <span data-ttu-id="1dc31-108">Nesse cenário, atualize os clientes App-V primeiro e, em seguida, atualize os componentes do servidor.</span><span class="sxs-lookup"><span data-stu-id="1dc31-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="1dc31-109">**Observação:** O App-V 4,6 tem saído do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="1dc31-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="1dc31-110">O App-V 5,0 oferece suporte somente a pacotes criados usando o App-V 5,0 ou pacotes que foram convertidos no formato App-V 5,0 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="1dc31-110">App-V 5.0 supports only packages that are created using App-V 5.0, or packages that have been converted to the App-V 5.0 (**.appv**) format.</span></span>

-   <span data-ttu-id="1dc31-111">App-V 5,0 SP3 somente: se você estiver atualizando o App-V Server do App-V 5,0 SP1, consulte [sobre o app-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="1dc31-111">App-V 5.0 SP3 only: If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3) for instructions.</span></span>

## <span data-ttu-id="1dc31-112">Executando o cliente App-V 5,0 simultaneamente com o App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="1dc31-112">Running the App-V 5.0 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="1dc31-113">Você pode executar o cliente App-V 5,0 simultaneamente no mesmo computador com o cliente App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="1dc31-113">You can run the App-V 5.0 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="1dc31-114">Ao executar clientes do App-V coexistentes, você pode:</span><span class="sxs-lookup"><span data-stu-id="1dc31-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="1dc31-115">Converta um pacote App-V 4,6 SP3 para o formato App-V 5,0 e publique ambos os pacotes, quando ambos os clientes estiverem em execução.</span><span class="sxs-lookup"><span data-stu-id="1dc31-115">Convert an App-V 4.6 SP3 package to the App-V 5.0 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="1dc31-116">Defina a política de migração para o pacote convertido, que permite que o pacote App-V 5,0 convertido assuma as associações de tipo de arquivo e atalhos do pacote App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="1dc31-116">Define the migration policy for the converted package, which allows the converted App-V 5.0 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="1dc31-117">Cenários de coexistência com suporte</span><span class="sxs-lookup"><span data-stu-id="1dc31-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="1dc31-118">A tabela a seguir mostra os cenários de coexistência do App-V com suporte.</span><span class="sxs-lookup"><span data-stu-id="1dc31-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="1dc31-119">Recomendamos que você instale as atualizações mais recentes disponíveis de uma determinada versão quando estiver executando clientes coexistentes.</span><span class="sxs-lookup"><span data-stu-id="1dc31-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1dc31-120">Tipo de cliente do App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="1dc31-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="1dc31-121">Tipo de cliente do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1dc31-121">App-V 5.0 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc31-122">App-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="1dc31-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc31-123">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1dc31-123">App-V 5.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc31-124">App-V 4,6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="1dc31-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dc31-125">App-V 5,0 RDS</span><span class="sxs-lookup"><span data-stu-id="1dc31-125">App-V 5.0 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1dc31-126">Requisitos para a execução de clientes coexistentes</span><span class="sxs-lookup"><span data-stu-id="1dc31-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="1dc31-127">Para executar clientes coexistentes, você deve:</span><span class="sxs-lookup"><span data-stu-id="1dc31-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="1dc31-128">Instale o cliente App-V 4.6 antes de instalar o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1dc31-128">Install the App-V4.6 client before you install the App-V 5.0 client.</span></span>

-   <span data-ttu-id="1dc31-129">Habilite a configuração da política de grupo **habilitar modo de migração** , que está no nó de coexistência do cliente **App-V** &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="1dc31-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="1dc31-130">Para obter o modelo. admx de implantação, consulte [como baixar e implantar modelos de política de grupo do MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="1dc31-130">To get the deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

### <span data-ttu-id="1dc31-131">Downloads e documentação do cliente</span><span class="sxs-lookup"><span data-stu-id="1dc31-131">Client downloads and documentation</span></span>

<span data-ttu-id="1dc31-132">A tabela a seguir fornece um link para a documentação do TechNet sobre as versões.</span><span class="sxs-lookup"><span data-stu-id="1dc31-132">The following table provides link to the TechNet documentation about the releases.</span></span> <span data-ttu-id="1dc31-133">A documentação do TechNet sobre o cliente App-V se aplica a ambos os clientes, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="1dc31-133">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1dc31-134">Versão do App-V</span><span class="sxs-lookup"><span data-stu-id="1dc31-134">App-V version</span></span></th>
<th align="left"><span data-ttu-id="1dc31-135">Link para a documentação do TechNet</span><span class="sxs-lookup"><span data-stu-id="1dc31-135">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dc31-136">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="1dc31-136">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="1dc31-137">Sobre o Microsoft Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="1dc31-137">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dc31-138">App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="1dc31-138">App-V 5.0SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-50-sp3.md" data-raw-source="[About Microsoft Application Virtualization 5.0 SP3](about-app-v-50-sp3.md)"><span data-ttu-id="1dc31-139">Sobre o Microsoft Application Virtualization 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="1dc31-139">About Microsoft Application Virtualization 5.0 SP3</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1dc31-140">Para obter mais informações sobre como configurar a coexistência do cliente do App-V 5,0, consulte:</span><span class="sxs-lookup"><span data-stu-id="1dc31-140">For more information about how to configure App-V 5.0 client coexistence, see:</span></span>

-   [<span data-ttu-id="1dc31-141">Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="1dc31-141">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

-   [<span data-ttu-id="1dc31-142">Coexistência e migração do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="1dc31-142">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="1dc31-143">Convertendo pacotes "versão anterior" usando o conversor de pacote</span><span class="sxs-lookup"><span data-stu-id="1dc31-143">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="1dc31-144">Antes de migrar um pacote, criado usando o App-V 4.6 SP3 ou anterior, para o App-V 5,0, examine os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="1dc31-144">Before migrating a package, created using App-V4.6SP3 or earlier, to App-V 5.0, review the following requirements:</span></span>

-   <span data-ttu-id="1dc31-145">Você deve converter o pacote para o formato de arquivo **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="1dc31-145">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="1dc31-146">O conversor de pacote dá suporte somente à conversão direta de pacotes que foram criados usando o App-V 4,5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="1dc31-146">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="1dc31-147">Para usar o conversor de pacote em um pacote criado com uma versão anterior, você deve usar uma versão App-V 4.5 ou posterior do sequenciador para atualizar o pacote e, em seguida, executar a conversão do pacote.</span><span class="sxs-lookup"><span data-stu-id="1dc31-147">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="1dc31-148">Para obter mais informações sobre como usar o conversor de pacote para converter um pacote, consulte [como converter um pacote criado em uma versão anterior do App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="1dc31-148">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md).</span></span> <span data-ttu-id="1dc31-149">Depois de converter o arquivo, você poderá implantá-lo em computadores de destino que executam o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="1dc31-149">After you convert the file, you can deploy it to target computers that run the App-V 5.0 client.</span></span>






## <span data-ttu-id="1dc31-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dc31-150">Related topics</span></span>


[<span data-ttu-id="1dc31-151">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="1dc31-151">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





