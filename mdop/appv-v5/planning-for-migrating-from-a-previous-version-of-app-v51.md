---
title: Planejamento para a migração de uma versão anterior do App-V
description: Planejamento para a migração de uma versão anterior do App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796257"
---
# <span data-ttu-id="04475-103">Planejamento para a migração de uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="04475-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="04475-104">Use as informações a seguir para planejar como migrar para o Microsoft Application Virtualization (App-V) 5,1 de versões anteriores do App-V.</span><span class="sxs-lookup"><span data-stu-id="04475-104">Use the following information to plan how to migrate to Microsoft Application Virtualization (App-V) 5.1 from previous versions of App-V.</span></span>

## <span data-ttu-id="04475-105">Requisitos de migração</span><span class="sxs-lookup"><span data-stu-id="04475-105">Migration requirements</span></span>


<span data-ttu-id="04475-106">Antes de iniciar qualquer atualização, examine os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="04475-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="04475-107">Se você estiver atualizando de uma versão anterior ao App-V 4,6 SP2, atualize para a versão App-V 4,6 SP3 primeiro antes de atualizar para o App-V 5,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="04475-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.1 or later.</span></span> <span data-ttu-id="04475-108">Nesse cenário, atualize os clientes App-V primeiro e, em seguida, atualize os componentes do servidor.</span><span class="sxs-lookup"><span data-stu-id="04475-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="04475-109">**Observação:** O App-V 4,6 tem saído do suporte básico.</span><span class="sxs-lookup"><span data-stu-id="04475-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="04475-110">O App-V 5,1 oferece suporte somente a pacotes criados usando o App-V 5,0 ou o App-V 5,1 ou pacotes que foram convertidos para o formato **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="04475-110">App-V 5.1 supports only packages that are created using App-V 5.0 or App-V 5.1, or packages that have been converted to the **.appv** format.</span></span>

-   <span data-ttu-id="04475-111">Se você estiver atualizando o App-V Server do App-V 5,0 SP1, consulte [sobre o app-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="04475-111">If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51) for instructions.</span></span>

## <span data-ttu-id="04475-112">Executando o cliente App-V 5,1 simultaneamente com o App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="04475-112">Running the App-V 5.1 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="04475-113">Você pode executar o cliente App-V 5,1 simultaneamente no mesmo computador com o cliente App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="04475-113">You can run the App-V 5.1 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="04475-114">Ao executar clientes do App-V coexistentes, você pode:</span><span class="sxs-lookup"><span data-stu-id="04475-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="04475-115">Converta um pacote App-V 4,6 SP3 para o formato App-V 5,1 e publique ambos os pacotes, quando ambos os clientes estiverem em execução.</span><span class="sxs-lookup"><span data-stu-id="04475-115">Convert an App-V 4.6 SP3 package to the App-V 5.1 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="04475-116">Defina a política de migração para o pacote convertido, que permite que o pacote App-V 5,1 convertido assuma as associações de tipo de arquivo e atalhos do pacote App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="04475-116">Define the migration policy for the converted package, which allows the converted App-V 5.1 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="04475-117">Cenários de coexistência com suporte</span><span class="sxs-lookup"><span data-stu-id="04475-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="04475-118">A tabela a seguir mostra os cenários de coexistência do App-V com suporte.</span><span class="sxs-lookup"><span data-stu-id="04475-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="04475-119">Recomendamos que você instale as atualizações mais recentes disponíveis de uma determinada versão quando estiver executando clientes coexistentes.</span><span class="sxs-lookup"><span data-stu-id="04475-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04475-120">Tipo de cliente do App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="04475-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="04475-121">Tipo de cliente do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="04475-121">App-V 5.1 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04475-122">App-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="04475-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="04475-123">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="04475-123">App-V 5.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04475-124">App-V 4,6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="04475-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="04475-125">App-V 5,1 RDS</span><span class="sxs-lookup"><span data-stu-id="04475-125">App-V 5.1 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="04475-126">Requisitos para a execução de clientes coexistentes</span><span class="sxs-lookup"><span data-stu-id="04475-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="04475-127">Para executar clientes coexistentes, você deve:</span><span class="sxs-lookup"><span data-stu-id="04475-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="04475-128">Instale o cliente App-V 4.6 antes de instalar o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="04475-128">Install the App-V4.6 client before you install the App-V 5.1 client.</span></span>

-   <span data-ttu-id="04475-129">Habilite a configuração da política de grupo **habilitar modo de migração** , que está no nó de coexistência do cliente **App-V** &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="04475-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="04475-130">Para implantar o modelo. admx, consulte [como baixar e implantar modelos de política de grupo do MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="04475-130">To deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

<span data-ttu-id="04475-131">**Observação**  Os pacotes do App-V 5,1 podem ser executados lado a lado com pacotes do App-V 4,6 se você tiver instalações coexistentes do App-V 5,1 e 4,6.</span><span class="sxs-lookup"><span data-stu-id="04475-131">**Note** App-V 5.1 packages can run side by side with App-V 4.6 packages if you have coexisting installations of App-V 5.1 and 4.6.</span></span> <span data-ttu-id="04475-132">No entanto, os pacotes do App-V 5,1 não podem interagir com pacotes do App-V 4,6 no mesmo ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="04475-132">However, App-V 5.1 packages cannot interact with App-V 4.6 packages in the same virtual environment.</span></span>

 

### <span data-ttu-id="04475-133">Downloads e documentação do cliente</span><span class="sxs-lookup"><span data-stu-id="04475-133">Client downloads and documentation</span></span>

<span data-ttu-id="04475-134">A tabela a seguir fornece links para os downloads do cliente App-V 4,6 e para a documentação do TechNet sobre as versões.</span><span class="sxs-lookup"><span data-stu-id="04475-134">The following table provides links to the App-V 4.6 client downloads and to the TechNet documentation about the releases.</span></span> <span data-ttu-id="04475-135">Os downloads incluem os clientes App-V "regular" e RDS.</span><span class="sxs-lookup"><span data-stu-id="04475-135">The downloads include the App-V “regular” and RDS clients.</span></span> <span data-ttu-id="04475-136">A documentação do TechNet sobre o cliente App-V se aplica a ambos os clientes, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="04475-136">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="04475-137">Versão do App-V</span><span class="sxs-lookup"><span data-stu-id="04475-137">App-V version</span></span></th>
<th align="left"><span data-ttu-id="04475-138">Link para a documentação do TechNet</span><span class="sxs-lookup"><span data-stu-id="04475-138">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04475-139">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="04475-139">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="04475-140">Sobre o Microsoft Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="04475-140">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04475-141">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="04475-141">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)"><span data-ttu-id="04475-142">Sobre o Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="04475-142">About Microsoft Application Virtualization 5.1</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="04475-143">Para obter mais informações sobre como configurar a coexistência do cliente do App-V 5,1, consulte:</span><span class="sxs-lookup"><span data-stu-id="04475-143">For more information about how to configure App-V 5.1 client coexistence, see:</span></span>

-   [<span data-ttu-id="04475-144">Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="04475-144">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [<span data-ttu-id="04475-145">Coexistência e migração do App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="04475-145">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="04475-146">Convertendo pacotes "versão anterior" usando o conversor de pacote</span><span class="sxs-lookup"><span data-stu-id="04475-146">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="04475-147">Antes de migrar um pacote, criado usando o aplicativo-4.6 SP2 ou anterior, para o App-V 5,1, examine os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="04475-147">Before migrating a package, created using App-4.6SP2 or earlier, to App-V 5.1, review the following requirements:</span></span>

-   <span data-ttu-id="04475-148">Você deve converter o pacote para o formato de arquivo **. AppV** .</span><span class="sxs-lookup"><span data-stu-id="04475-148">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="04475-149">O conversor de pacote dá suporte somente à conversão direta de pacotes que foram criados usando o App-V 4,5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="04475-149">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="04475-150">Para usar o conversor de pacote em um pacote criado com uma versão anterior, você deve usar uma versão App-V 4.5 ou posterior do sequenciador para atualizar o pacote e, em seguida, executar a conversão do pacote.</span><span class="sxs-lookup"><span data-stu-id="04475-150">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="04475-151">Para obter mais informações sobre como usar o conversor de pacote para converter um pacote, consulte [como converter um pacote criado em uma versão anterior do App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="04475-151">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span></span> <span data-ttu-id="04475-152">Depois de converter o arquivo, você poderá implantá-lo em computadores de destino que executam o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="04475-152">After you convert the file, you can deploy it to target computers that run the App-V 5.1 client.</span></span>






## <span data-ttu-id="04475-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04475-153">Related topics</span></span>


[<span data-ttu-id="04475-154">Planejando a implantação do App-V</span><span class="sxs-lookup"><span data-stu-id="04475-154">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





