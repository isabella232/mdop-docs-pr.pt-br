---
title: Migrando para o App-V 5.1 de uma versão anterior
description: Migrando para o App-V 5.1 de uma versão anterior
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796278"
---
# <span data-ttu-id="6a2cc-103">Migrando para o App-V 5.1 de uma versão anterior</span><span class="sxs-lookup"><span data-stu-id="6a2cc-103">Migrating to App-V 5.1 from a Previous Version</span></span>


<span data-ttu-id="6a2cc-104">Com o Microsoft Application Virtualization (App-V) 5,1, você pode migrar sua infraestrutura existente do App-V 4,6 ou App-V 5,0 para a infraestrutura mais flexível, integrada e mais fácil de gerenciar do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-104">With Microsoft Application Virtualization (App-V) 5.1, you can migrate your existing App-V 4.6 or App-V 5.0 infrastructure to the more flexible, integrated, and easier to manage App-V 5.1 infrastructure.</span></span>
<span data-ttu-id="6a2cc-105">No entanto, não é possível migrar diretamente do App-V 4. x para o App-V 5,1, você deve migrar para o App-V 5,0 primeiro.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-105">However, you cannot migrate directly from App-V 4.x to App-V 5.1, you must migrate to App-V 5.0 first.</span></span> <span data-ttu-id="6a2cc-106">Para obter mais informações sobre como migrar do App-V 4. x para o App-V 5,0, confira [migrar de uma versão anterior](migrating-from-a-previous-version-app-v-50.md)</span><span class="sxs-lookup"><span data-stu-id="6a2cc-106">For more information on migrating from App-V 4.x to App-V 5.0, see [Migrating from a Previous Version](migrating-from-a-previous-version-app-v-50.md)</span></span>  

<span data-ttu-id="6a2cc-107">**Observação**  Os pacotes do App-V 5,1 são exatamente iguais aos pacotes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-107">**Note** App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="6a2cc-108">Não houve nenhuma alteração no formato do pacote entre as versões e, portanto, não há necessidade de converter pacotes do App-V 5,0 para pacotes do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-108">There has been no change in the package format between the versions and therefore, there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>

<span data-ttu-id="6a2cc-109">Para obter mais informações sobre as diferenças entre o App-V 4,6 e o App-V 5,1, consulte a **seção diferenças entre o app-v 4,6 e o app-v 5,0** de [sobre o app-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="6a2cc-109">For more information about the differences between App-V 4.6 and App-V 5.1, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="6a2cc-110">Melhorias no conversor de pacotes do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="6a2cc-110">Improvements to the App-V 5.1 Package Converter</span></span>


<span data-ttu-id="6a2cc-111">Agora você pode usar o conversor de pacote para converter pacotes do App-V 4,6 que contêm scripts e informações do registro e scripts dos arquivos Source. OSD agora estão incluídos na saída do conversor de pacote.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-111">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="6a2cc-112">Você também pode usar o `–OSDsToIncludeInPackage` parâmetro com o `ConvertFrom-AppvLegacyPackage` cmdlet para especificar quais informações de arquivos. OSD são convertidas e colocadas dentro do novo pacote.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-112">You can also use the `–OSDsToIncludeInPackage` parameter with the `ConvertFrom-AppvLegacyPackage` cmdlet to specify which .osd files’ information is converted and placed within the new package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a2cc-113">Novo no App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="6a2cc-113">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="6a2cc-114">Antes do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="6a2cc-114">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a2cc-115">Os novos arquivos. XML são criados correspondentes aos arquivos. OSD associados a um pacote; esses arquivos incluem as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="6a2cc-115">New .xml files are created corresponding to the .osd files associated with a package; these files include the following information:</span></span></p>
<ul>
<li><p><span data-ttu-id="6a2cc-116">variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="6a2cc-116">environment variables</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-117">teclado</span><span class="sxs-lookup"><span data-stu-id="6a2cc-117">shortcuts</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-118">associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="6a2cc-118">file type associations</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-119">informações do registro</span><span class="sxs-lookup"><span data-stu-id="6a2cc-119">registry information</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-120">escritas</span><span class="sxs-lookup"><span data-stu-id="6a2cc-120">scripts</span></span></p></li>
</ul>
<p><span data-ttu-id="6a2cc-121">Agora você pode optar por adicionar informações de um subconjunto de arquivos. OSD no diretório de origem ao pacote usando o <code>-OSDsToIncludeInPackage</code> parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-121">You can now choose to add information from a subset of the .osd files in the source directory to the package using the <code>-OSDsToIncludeInPackage</code> parameter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a2cc-122">As informações do registro e os scripts incluídos nos arquivos. OSD associados a um pacote não foram incluídos na saída do conversor de pacote.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-122">Registry information and scripts included in .osd files associated with a package were not included in package converter output.</span></span></p>
<p><span data-ttu-id="6a2cc-123">O conversor de pacote preencheria o novo pacote com informações de todos os arquivos. OSD no diretório de origem.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-123">The package converter would populate the new package with information from all of the .osd files in the source directory.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="6a2cc-124">Exemplo de instrução de conversão</span><span class="sxs-lookup"><span data-stu-id="6a2cc-124">Example conversion statement</span></span>

<span data-ttu-id="6a2cc-125">Para entender o novo processo, examine a seguinte instrução do conversor de pacote de exemplo `ConvertFrom-AppvLegacyPackage` .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-125">To understand the new process, review the following example `ConvertFrom-AppvLegacyPackage` package converter statement.</span></span>

**<span data-ttu-id="6a2cc-126">Se o diretório de origem (\\\\OldPkgStore\\ContosoApp) incluir o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6a2cc-126">If the source directory (\\\\OldPkgStore\\ContosoApp) includes the following:</span></span>**

-   <span data-ttu-id="6a2cc-127">ContosoApp. SFT</span><span class="sxs-lookup"><span data-stu-id="6a2cc-127">ContosoApp.sft</span></span>

-   <span data-ttu-id="6a2cc-128">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="6a2cc-128">ContosoApp.msi</span></span>

-   <span data-ttu-id="6a2cc-129">ContosoApp.sprj</span><span class="sxs-lookup"><span data-stu-id="6a2cc-129">ContosoApp.sprj</span></span>

-   <span data-ttu-id="6a2cc-130">ContosoApp\_manifest.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-130">ContosoApp\_manifest.xml</span></span>

-   <span data-ttu-id="6a2cc-131">X. OSD</span><span class="sxs-lookup"><span data-stu-id="6a2cc-131">X.osd</span></span>

-   <span data-ttu-id="6a2cc-132">S. OSD</span><span class="sxs-lookup"><span data-stu-id="6a2cc-132">Y.osd</span></span>

-   <span data-ttu-id="6a2cc-133">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="6a2cc-133">Z.osd</span></span>

**<span data-ttu-id="6a2cc-134">E executar este comando:</span><span class="sxs-lookup"><span data-stu-id="6a2cc-134">And you run this command:</span></span>**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**<span data-ttu-id="6a2cc-135">O seguinte é criado no diretório de destino (\\\\NewPkgStore\\ContosoApp):</span><span class="sxs-lookup"><span data-stu-id="6a2cc-135">The following is created in the destination directory (\\\\NewPkgStore\\ContosoApp):</span></span>**

-   <span data-ttu-id="6a2cc-136">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="6a2cc-136">ContosoApp.appv</span></span>

-   <span data-ttu-id="6a2cc-137">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="6a2cc-137">ContosoApp.msi</span></span>

-   <span data-ttu-id="6a2cc-138">ContosoApp\_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-138">ContosoApp\_DeploymentConfig.xml</span></span>

-   <span data-ttu-id="6a2cc-139">ContosoApp\_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-139">ContosoApp\_UserConfig.xml</span></span>

-   <span data-ttu-id="6a2cc-140">X\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-140">X\_Config.xml</span></span>

-   <span data-ttu-id="6a2cc-141">Y\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-141">Y\_Config.xml</span></span>

-   <span data-ttu-id="6a2cc-142">Z\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-142">Z\_Config.xml</span></span>

**<span data-ttu-id="6a2cc-143">No exemplo acima:</span><span class="sxs-lookup"><span data-stu-id="6a2cc-143">In the above example:</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a2cc-144">Estes arquivos de diretório de origem...</span><span class="sxs-lookup"><span data-stu-id="6a2cc-144">These Source directory files…</span></span></th>
<th align="left"><span data-ttu-id="6a2cc-145">... são convertidos nestes arquivos de diretório de destino...</span><span class="sxs-lookup"><span data-stu-id="6a2cc-145">…are converted to these Destination directory files…</span></span></th>
<th align="left"><span data-ttu-id="6a2cc-146">... e conterá esses itens</span><span class="sxs-lookup"><span data-stu-id="6a2cc-146">…and will contain these items</span></span></th>
<th align="left"><span data-ttu-id="6a2cc-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a2cc-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="6a2cc-148">X. OSD</span><span class="sxs-lookup"><span data-stu-id="6a2cc-148">X.osd</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-149">S. OSD</span><span class="sxs-lookup"><span data-stu-id="6a2cc-149">Y.osd</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-150">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="6a2cc-150">Z.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6a2cc-151">X_Config.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-151">X_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-152">Y_Config.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-152">Y_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-153">Z_Config.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-153">Z_Config.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6a2cc-154">Variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="6a2cc-154">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-155">Teclado</span><span class="sxs-lookup"><span data-stu-id="6a2cc-155">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-156">Associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="6a2cc-156">File type associations</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-157">Informações do registro</span><span class="sxs-lookup"><span data-stu-id="6a2cc-157">Registry information</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-158">Scripts</span><span class="sxs-lookup"><span data-stu-id="6a2cc-158">Scripts</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="6a2cc-159">Cada arquivo. OSD é convertido em um arquivo. xml separado e correspondente que contém os itens listados aqui no formato de configuração de implantação do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-159">Each .osd file is converted to a separate, corresponding .xml file that contains the items listed here in App-V 5.1 deployment configuration format.</span></span> <span data-ttu-id="6a2cc-160">Esses itens podem ser copiados desses arquivos. xml e colocados na configuração de implantação ou arquivos de configuração do usuário, conforme desejado.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-160">These items can then be copied from these .xml files and placed in the deployment configuration or user configuration files as desired.</span></span></p>
<p><span data-ttu-id="6a2cc-161">Neste exemplo, há três arquivos. xml, correspondentes aos três arquivos. OSD no diretório de origem.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-161">In this example, there are three .xml files, corresponding with the three .osd files in the source directory.</span></span> <span data-ttu-id="6a2cc-162">Cada arquivo. xml contém as variáveis de ambiente, atalhos, associações de tipo de arquivo, informações do registro e scripts em seu arquivo. OSD correspondente.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-162">Each .xml file contains the environment variables, shortcuts, file type associations, registry information, and scripts in its corresponding .osd file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="6a2cc-163">X. OSD</span><span class="sxs-lookup"><span data-stu-id="6a2cc-163">X.osd</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-164">S. OSD</span><span class="sxs-lookup"><span data-stu-id="6a2cc-164">Y.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6a2cc-165">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="6a2cc-165">ContosoApp.appv</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-166">ContosoApp_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-166">ContosoApp_DeploymentConfig.xml</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-167">ContosoApp_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="6a2cc-167">ContosoApp_UserConfig.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="6a2cc-168">Variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="6a2cc-168">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-169">Teclado</span><span class="sxs-lookup"><span data-stu-id="6a2cc-169">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="6a2cc-170">Associações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="6a2cc-170">File type associations</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="6a2cc-171">As informações dos arquivos. OSD especificadas no <code>-OSDsToIncludeInPackage</code> parâmetro são convertidas e colocadas dentro do pacote.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-171">The information from the .osd files specified in the <code>-OSDsToIncludeInPackage</code> parameter are converted and placed inside the package.</span></span> <span data-ttu-id="6a2cc-172">Em seguida, o conversor preenche o arquivo de configuração de implantação e o arquivo de configuração do usuário com o conteúdo do pacote, da mesma forma que o sequenciador do App-V faz ao sequenciar um novo pacote.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-172">The converter then populates the deployment configuration file and the user configuration file with the contents of the package, just as App-V Sequencer does when sequencing a new package.</span></span></p>
<p><span data-ttu-id="6a2cc-173">Neste exemplo, as variáveis de ambiente, atalhos e associações de tipo de arquivo incluídas em X. OSD e Y. OSD foram convertidos e colocados no pacote App-V, e algumas dessas informações também foram incluídas nos arquivos de configuração de implantação e configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-173">In this example, environment variables, shortcuts, and file type associations included in X.osd and Y.osd were converted and placed in the App-V package, and some of this information was also included in the deployment configuration and user configuration files.</span></span> <span data-ttu-id="6a2cc-174">X. OSD e Y. OSD foram usados porque foram incluídos como argumentos para o <code>-OSDsToIncludeInPackage</code> parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-174">X.osd and Y.osd were used because they were included as arguments to the <code>-OSDsToIncludeInPackage</code> parameter.</span></span> <span data-ttu-id="6a2cc-175">Nenhuma informação do Z. OSD foi incluída no pacote porque não foi incluída como um desses argumentos.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-175">No information from Z.osd was included in the package, because it was not included as one of these arguments.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6a2cc-176">Convertendo pacotes criados usando uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="6a2cc-176">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="6a2cc-177">Use o utilitário conversor de pacote para atualizar pacotes de aplicativos virtuais criados usando versões do App-V antes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-177">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="6a2cc-178">O conversor de pacote usa o PowerShell para converter pacotes e pode ajudar a automatizar o processo se você tiver muitos pacotes que exijam conversão.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-178">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="6a2cc-179">**Importante**  Depois de converter um pacote existente, você deve testar o pacote antes de implantar o pacote para garantir que o processo de conversão foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-179">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="6a2cc-180">O que saber antes de converter pacotes existentes</span><span class="sxs-lookup"><span data-stu-id="6a2cc-180">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a2cc-181">Problema</span><span class="sxs-lookup"><span data-stu-id="6a2cc-181">Issue</span></span></th>
<th align="left"><span data-ttu-id="6a2cc-182">Solução alternativa</span><span class="sxs-lookup"><span data-stu-id="6a2cc-182">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a2cc-183">Os pacotes virtuais que usam o DSC não são vinculados após a conversão.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-183">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a2cc-184">Vincule os pacotes usando grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-184">Link the packages using connection groups.</span></span> <span data-ttu-id="6a2cc-185">Consulte <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> Gerenciando grupos de conexão </a> .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-185">See <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a2cc-186">Conflitos de variáveis de ambiente são detectados durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-186">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a2cc-187">Resolva os conflitos no <strong> arquivo. OSD associado </strong> .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-187">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a2cc-188">Caminhos de código fixo são detectados durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-188">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a2cc-189">Os caminhos embutidos em código são difíceis de serem convertidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-189">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="6a2cc-190">O conversor de pacote detecta e retorna pacotes com arquivos que contêm caminhos embutidos em código.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-190">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="6a2cc-191">Exiba o arquivo com o caminho embutido e determine se o pacote requer o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-191">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="6a2cc-192">Em caso afirmativo, é recomendável resequenciar o pacote.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-192">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6a2cc-193">Ao converter um pacote, verifique se há arquivos ou atalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-193">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="6a2cc-194">Localize o item no pacote App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-194">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="6a2cc-195">Pode ser um caminho embutido em código.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-195">It could possibly be a hard-coded path.</span></span> <span data-ttu-id="6a2cc-196">Converter o caminho.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-196">Convert the path.</span></span>

<span data-ttu-id="6a2cc-197">**Observação**  É recomendável que você use o sequenciador do App-V 5,1 para converter aplicativos críticos ou aplicativos que precisam tirar proveito dos recursos.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-197">**Note** It is recommended that you use the App-V 5.1 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="6a2cc-198">Veja [como sequenciar um novo aplicativo com o App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="6a2cc-198">See, [How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span></span>

<span data-ttu-id="6a2cc-199">Se um pacote convertido não abrir após você convertê-lo, também é recomendável que você reaplique a sequência do aplicativo usando o sequenciador do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-199">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.1 sequencer.</span></span>

 

[<span data-ttu-id="6a2cc-200">Como converter um pacote criado em uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="6a2cc-200">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## <span data-ttu-id="6a2cc-201">Migrando clientes</span><span class="sxs-lookup"><span data-stu-id="6a2cc-201">Migrating Clients</span></span>


<span data-ttu-id="6a2cc-202">A tabela a seguir exibe o método recomendado para a atualização de clientes.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-202">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a2cc-203">Tarefa</span><span class="sxs-lookup"><span data-stu-id="6a2cc-203">Task</span></span></th>
<th align="left"><span data-ttu-id="6a2cc-204">Mais informações</span><span class="sxs-lookup"><span data-stu-id="6a2cc-204">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a2cc-205">Atualize seu ambiente para a versão mais recente do App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="6a2cc-205">Upgrade your environment to the latest version of App-V4.6</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="6a2cc-206">Considerações de atualização e implantação do Application Virtualization </a> .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-206">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a2cc-207">Instale o cliente do App-V 5,1 com coexistência habilitada.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-207">Install the App-V 5.1 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)"><span data-ttu-id="6a2cc-208">Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador </a> .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-208">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a2cc-209">Sequenciar e distribuir pacotes do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-209">Sequence and roll out App-V 5.1 packages.</span></span> <span data-ttu-id="6a2cc-210">Conforme necessário, cancele a publicação de pacotes do App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-210">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)"><span data-ttu-id="6a2cc-211">Como sequenciar um novo aplicativo com o App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-211">How to Sequence a New Application with App-V 5.1</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6a2cc-212">**Importante**  Você deve estar executando a versão mais recente do App-V 4.6 para usar o modo de coexistência.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-212">**Important** You must be running the latest version of App-V4.6 to use coexistence mode.</span></span> <span data-ttu-id="6a2cc-213">Além disso, quando você sequenciar um pacote, você deve definir a configuração de **autoridade de gerenciamento** , que está localizada na seção **configuração do usuário** .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-213">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="6a2cc-214">Migrando a infraestrutura completa do App-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="6a2cc-214">Migrating the App-V 5.1 Server Full Infrastructure</span></span>


<span data-ttu-id="6a2cc-215">Não há um método direto para atualizar para uma infraestrutura completa do App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-215">There is no direct method to upgrade to a full App-V 5.1 infrastructure.</span></span> <span data-ttu-id="6a2cc-216">Use as informações na seção a seguir para obter informações sobre como atualizar o servidor App-V.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-216">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a2cc-217">Tarefa</span><span class="sxs-lookup"><span data-stu-id="6a2cc-217">Task</span></span></th>
<th align="left"><span data-ttu-id="6a2cc-218">Mais informações</span><span class="sxs-lookup"><span data-stu-id="6a2cc-218">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a2cc-219">Atualize seu ambiente para a versão mais recente do App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-219">Upgrade your environment to the latest version of App-V4.6.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="6a2cc-220">Considerações de atualização e implantação do Application Virtualization </a> .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-220">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a2cc-221">Implante a versão do App-V 5,1 do cliente.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-221">Deploy App-V 5.1 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="6a2cc-222">Como implantar o cliente App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-222">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a2cc-223">Instale o App-V 5,1 Server.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-223">Install App-V 5.1 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="6a2cc-224">Como implantar o servidor do App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="6a2cc-224">How to Deploy the App-V 5.1 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a2cc-225">Migrar pacotes existentes.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-225">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a2cc-226">Veja a <strong> seção convertendo pacotes criados usando uma versão anterior do App-V </strong> deste artigo.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-226">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6a2cc-227">Tarefas de migração adicionais</span><span class="sxs-lookup"><span data-stu-id="6a2cc-227">Additional Migration tasks</span></span>


<span data-ttu-id="6a2cc-228">Você também pode executar tarefas de migração adicionais, como reconfiguração de pontos de extremidade, bem como abrir um pacote criado usando uma versão anterior em um computador que executa o cliente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-228">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.1 client.</span></span> <span data-ttu-id="6a2cc-229">Os links a seguir fornecem mais informações sobre como executar essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="6a2cc-229">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="6a2cc-230">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 convertido para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="6a2cc-230">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="6a2cc-231">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="6a2cc-231">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[<span data-ttu-id="6a2cc-232">Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="6a2cc-232">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="6a2cc-233">Como reverter pontos de extensão de um pacote do App-V 5.1 para um pacote do App-V 4.6 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="6a2cc-233">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="6a2cc-234">Outros recursos para executar tarefas de migração do App-V</span><span class="sxs-lookup"><span data-stu-id="6a2cc-234">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="6a2cc-235">Operações para o App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="6a2cc-235">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="6a2cc-236">Um procedimento simplificado de atualização do servidor de gerenciamento do Microsoft App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="6a2cc-236">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





