---
title: Migração de uma versão anterior
description: Migração de uma versão anterior
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796279"
---
# <span data-ttu-id="167f5-103">Migração de uma versão anterior</span><span class="sxs-lookup"><span data-stu-id="167f5-103">Migrating from a Previous Version</span></span>


<span data-ttu-id="167f5-104">Com o App-V 5,0, você pode migrar sua infraestrutura existente do App-V 4,6 para a infraestrutura mais flexível, integrada e mais fácil de gerenciar do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="167f5-104">With App-V 5.0 you can migrate your existing App-V 4.6 infrastructure to the more flexible, integrated, and easier to manage App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="167f5-105">Considere as seguintes seções quando planejar a estratégia de migração:</span><span class="sxs-lookup"><span data-stu-id="167f5-105">Consider the following sections when you plan your migration strategy:</span></span>

<span data-ttu-id="167f5-106">**Observação**  Para obter mais informações sobre as diferenças entre o App-V 4,6 e o App-V 5,0, consulte a **seção diferenças entre o app-v 4,6 e o app-v 5,0** de [sobre o app-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="167f5-106">**Note** For more information about the differences between App-V 4.6 and App-V 5.0, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <span data-ttu-id="167f5-107">Convertendo pacotes criados usando uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="167f5-107">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="167f5-108">Use o utilitário conversor de pacote para atualizar pacotes de aplicativos virtuais criados usando versões anteriores do App-V.</span><span class="sxs-lookup"><span data-stu-id="167f5-108">Use the package converter utility to upgrade virtual application packages created using previous versions of App-V.</span></span> <span data-ttu-id="167f5-109">O conversor de pacote usa o PowerShell para converter pacotes e pode ajudar a automatizar o processo se você tiver muitos pacotes que exijam conversão.</span><span class="sxs-lookup"><span data-stu-id="167f5-109">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="167f5-110">**Importante**  Depois de converter um pacote existente, você deve testar o pacote antes de implantar o pacote para garantir que o processo de conversão foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="167f5-110">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="167f5-111">O que saber antes de converter pacotes existentes</span><span class="sxs-lookup"><span data-stu-id="167f5-111">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="167f5-112">Problema</span><span class="sxs-lookup"><span data-stu-id="167f5-112">Issue</span></span></th>
<th align="left"><span data-ttu-id="167f5-113">Solução alternativa</span><span class="sxs-lookup"><span data-stu-id="167f5-113">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="167f5-114">Os scripts de pacote não são convertidos.</span><span class="sxs-lookup"><span data-stu-id="167f5-114">Package scripts are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="167f5-115">Testar o pacote convertido.</span><span class="sxs-lookup"><span data-stu-id="167f5-115">Test the converted package.</span></span> <span data-ttu-id="167f5-116">Se necessário, converta o script.</span><span class="sxs-lookup"><span data-stu-id="167f5-116">If necessary convert the script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="167f5-117">As substituições de configuração do registro do pacote não são convertidas.</span><span class="sxs-lookup"><span data-stu-id="167f5-117">Package registry setting overrides are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="167f5-118">Testar o pacote convertido.</span><span class="sxs-lookup"><span data-stu-id="167f5-118">Test the converted package.</span></span> <span data-ttu-id="167f5-119">Se necessário, adicione novamente as substituições do registro.</span><span class="sxs-lookup"><span data-stu-id="167f5-119">If necessary, re-add registry overrides.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="167f5-120">Os pacotes virtuais que usam o DSC não são vinculados após a conversão.</span><span class="sxs-lookup"><span data-stu-id="167f5-120">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="167f5-121">Vincule os pacotes usando grupos de conexão.</span><span class="sxs-lookup"><span data-stu-id="167f5-121">Link the packages using connection groups.</span></span> <span data-ttu-id="167f5-122">Consulte <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> Gerenciando grupos de conexão </a> .</span><span class="sxs-lookup"><span data-stu-id="167f5-122">See <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="167f5-123">Conflitos de variáveis de ambiente são detectados durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="167f5-123">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="167f5-124">Resolva os conflitos no <strong> arquivo. OSD associado </strong> .</span><span class="sxs-lookup"><span data-stu-id="167f5-124">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="167f5-125">Caminhos de código fixo são detectados durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="167f5-125">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="167f5-126">Os caminhos embutidos em código são difíceis de serem convertidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="167f5-126">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="167f5-127">O conversor de pacote detecta e retorna pacotes com arquivos que contêm caminhos embutidos em código.</span><span class="sxs-lookup"><span data-stu-id="167f5-127">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="167f5-128">Exiba o arquivo com o caminho embutido e determine se o pacote requer o arquivo.</span><span class="sxs-lookup"><span data-stu-id="167f5-128">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="167f5-129">Em caso afirmativo, é recomendável resequenciar o pacote.</span><span class="sxs-lookup"><span data-stu-id="167f5-129">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="167f5-130">Ao converter um pacote, verifique se há arquivos ou atalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="167f5-130">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="167f5-131">Localize o item no pacote App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="167f5-131">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="167f5-132">Pode ser um caminho embutido.</span><span class="sxs-lookup"><span data-stu-id="167f5-132">It could possibly be hard-coded path.</span></span> <span data-ttu-id="167f5-133">Converter o caminho.</span><span class="sxs-lookup"><span data-stu-id="167f5-133">Convert the path.</span></span>

<span data-ttu-id="167f5-134">**Observação**  É recomendável que você use o sequenciador do App-V 5,0 para converter aplicativos críticos ou aplicativos que precisam tirar proveito dos recursos.</span><span class="sxs-lookup"><span data-stu-id="167f5-134">**Note** It is recommended that you use the App-V 5.0 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="167f5-135">Veja [como sequenciar um novo aplicativo com o App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="167f5-135">See, [How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span></span>

<span data-ttu-id="167f5-136">Se um pacote convertido não abrir após você convertê-lo, também é recomendável que você reaplique a sequência do aplicativo usando o sequenciador do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="167f5-136">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.0 sequencer.</span></span>

 

[<span data-ttu-id="167f5-137">Como converter um pacote criado em uma versão anterior do App-V</span><span class="sxs-lookup"><span data-stu-id="167f5-137">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## <span data-ttu-id="167f5-138">Migrando clientes</span><span class="sxs-lookup"><span data-stu-id="167f5-138">Migrating Clients</span></span>


<span data-ttu-id="167f5-139">A tabela a seguir exibe o método recomendado para a atualização de clientes.</span><span class="sxs-lookup"><span data-stu-id="167f5-139">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="167f5-140">Tarefa</span><span class="sxs-lookup"><span data-stu-id="167f5-140">Task</span></span></th>
<th align="left"><span data-ttu-id="167f5-141">Mais informações</span><span class="sxs-lookup"><span data-stu-id="167f5-141">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="167f5-142">Atualizar seu ambiente para o App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="167f5-142">Upgrade your environment to App-V4.6SP2</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="167f5-143">Considerações de atualização e implantação do Application Virtualization </a> .</span><span class="sxs-lookup"><span data-stu-id="167f5-143">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="167f5-144">Instale o cliente do App-V 5,0 com coexistência habilitada.</span><span class="sxs-lookup"><span data-stu-id="167f5-144">Install the App-V 5.0 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)"><span data-ttu-id="167f5-145">Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador </a> .</span><span class="sxs-lookup"><span data-stu-id="167f5-145">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="167f5-146">Sequenciar e distribuir pacotes do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="167f5-146">Sequence and roll out App-V 5.0 packages.</span></span> <span data-ttu-id="167f5-147">Conforme necessário, cancele a publicação de pacotes do App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="167f5-147">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)"><span data-ttu-id="167f5-148">Como sequenciar um novo aplicativo com o App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="167f5-148">How to Sequence a New Application with App-V 5.0</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="167f5-149">**Importante**  Você deve estar executando o App-V 4.6 SP3 para usar o modo de coexistência.</span><span class="sxs-lookup"><span data-stu-id="167f5-149">**Important** You must be running App-V4.6SP3 to use coexistence mode.</span></span> <span data-ttu-id="167f5-150">Além disso, quando você sequenciar um pacote, você deve definir a configuração de **autoridade de gerenciamento** , que está localizada na seção **configuração do usuário** .</span><span class="sxs-lookup"><span data-stu-id="167f5-150">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="167f5-151">Migrando a infraestrutura completa do App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="167f5-151">Migrating the App-V 5.0 Server Full Infrastructure</span></span>


<span data-ttu-id="167f5-152">Não há um método direto para atualizar para uma infraestrutura completa do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="167f5-152">There is no direct method to upgrade to a full App-V 5.0 infrastructure.</span></span> <span data-ttu-id="167f5-153">Use as informações na seção a seguir para obter informações sobre como atualizar o servidor App-V.</span><span class="sxs-lookup"><span data-stu-id="167f5-153">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="167f5-154">Tarefa</span><span class="sxs-lookup"><span data-stu-id="167f5-154">Task</span></span></th>
<th align="left"><span data-ttu-id="167f5-155">Mais informações</span><span class="sxs-lookup"><span data-stu-id="167f5-155">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="167f5-156">Atualize seu ambiente para o App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="167f5-156">Upgrade your environment to App-V4.6SP3.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="167f5-157">Considerações de atualização e implantação do Application Virtualization </a> .</span><span class="sxs-lookup"><span data-stu-id="167f5-157">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="167f5-158">Implante a versão do App-V 5,0 do cliente.</span><span class="sxs-lookup"><span data-stu-id="167f5-158">Deploy App-V 5.0 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="167f5-159">Como implantar o cliente App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="167f5-159">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="167f5-160">Instale o App-V 5,0 Server.</span><span class="sxs-lookup"><span data-stu-id="167f5-160">Install App-V 5.0 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="167f5-161">Como implantar o servidor do App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="167f5-161">How to Deploy the App-V 5.0 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="167f5-162">Migrar pacotes existentes.</span><span class="sxs-lookup"><span data-stu-id="167f5-162">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="167f5-163">Veja a <strong> seção convertendo pacotes criados usando uma versão anterior do App-V </strong> deste artigo.</span><span class="sxs-lookup"><span data-stu-id="167f5-163">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="167f5-164">Tarefas de migração adicionais</span><span class="sxs-lookup"><span data-stu-id="167f5-164">Additional Migration tasks</span></span>


<span data-ttu-id="167f5-165">Você também pode executar tarefas de migração adicionais, como reconfiguração de pontos de extremidade, bem como abrir um pacote criado usando uma versão anterior em um computador que executa o cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="167f5-165">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.0 client.</span></span> <span data-ttu-id="167f5-166">Os links a seguir fornecem mais informações sobre como executar essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="167f5-166">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="167f5-167">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="167f5-167">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="167f5-168">Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="167f5-168">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[<span data-ttu-id="167f5-169">Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para todos os usuários em um computador específico</span><span class="sxs-lookup"><span data-stu-id="167f5-169">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="167f5-170">Como reverter pontos de extensão de um pacote do App-V 5.0 para um pacote do App-V 4.6 para um usuário específico</span><span class="sxs-lookup"><span data-stu-id="167f5-170">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="167f5-171">Outros recursos para executar tarefas de migração do App-V</span><span class="sxs-lookup"><span data-stu-id="167f5-171">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="167f5-172">Operações para o App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="167f5-172">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="167f5-173">Um procedimento simplificado de atualização do servidor de gerenciamento do Microsoft App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="167f5-173">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





