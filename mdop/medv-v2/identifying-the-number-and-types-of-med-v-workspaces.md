---
title: Identificação do número e dos tipos de espaços de trabalho da MED-V
description: Identificação do número e dos tipos de espaços de trabalho da MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800037"
---
# <span data-ttu-id="1cd83-103">Identificação do número e dos tipos de espaços de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="1cd83-103">Identifying the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="1cd83-104">O MED-V cria um ambiente virtual para executar aplicativos que exijam o Windows XP ou que exijam uma versão do Internet Explorer diferente da versão do computador host.</span><span class="sxs-lookup"><span data-stu-id="1cd83-104">MED-V creates a virtual environment for running applications that require Windows XP or that require a version of Internet Explorer that differs from the version on the host computer.</span></span> <span data-ttu-id="1cd83-105">Esse ambiente virtual é conhecido como um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-105">This virtual environment is known as a MED-V workspace.</span></span>

<span data-ttu-id="1cd83-106">Dependendo dos requisitos de compatibilidade do aplicativo enfrentados pela sua organização durante a migração para o Windows 7, apenas determinados usuários ou departamentos podem exigir espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-106">Depending on the application compatibility requirements faced by your organization as you migrate to Windows 7, only certain users or departments might require MED-V workspaces.</span></span> <span data-ttu-id="1cd83-107">Ao planejar sua implantação, você precisa determinar o número de espaços de trabalho do MED-V necessários na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="1cd83-107">As you plan your deployment, you have to determine the number of MED-V workspaces required in your enterprise.</span></span> <span data-ttu-id="1cd83-108">Você também precisa definir os requisitos de cada espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-108">You also have to define the requirements of each MED-V workspace.</span></span>

## <span data-ttu-id="1cd83-109">Identificar o número e os tipos de espaços de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1cd83-109">Identify the Number and Types of MED-V Workspaces</span></span>


<span data-ttu-id="1cd83-110">Identifique os computadores e grupos da sua empresa para os quais você criará os espaços de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-110">Identify the computers and groups in your enterprise for which you will be creating MED-V workspaces.</span></span> <span data-ttu-id="1cd83-111">Geralmente, estes são os usuários que precisam de acesso a esses aplicativos que não podem ser migrados para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cd83-111">Typically, these are the users who require access to those applications that cannot be migrated to Windows 7.</span></span> <span data-ttu-id="1cd83-112">Identifique os aplicativos que não podem ser migrados e os usuários que precisam de um espaço de trabalho do MED-V para executar esses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1cd83-112">Identify those applications that cannot be migrated and the users who require a MED-V workspace to run these applications.</span></span>

<span data-ttu-id="1cd83-113">Você também pode ter endereços de intranet que ainda não foram otimizados para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cd83-113">You might also have intranet addresses that have not yet been optimized for Windows 7.</span></span> <span data-ttu-id="1cd83-114">O espaço de trabalho do MED-V fornece um navegador do Internet Explorer pelo qual os usuários finais podem acessar melhor os endereços da Web que ainda não estão prontos para a migração para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cd83-114">The MED-V workspace provides an Internet Explorer browser through which end users can better access those web addresses that are not yet ready for the migration to Windows 7.</span></span> <span data-ttu-id="1cd83-115">À medida que você estiver preparando e planejando a implantação do MED-V, será preciso identificar e compilar uma lista dos endereços de URL para redirecionar do Internet Explorer no computador host para o Internet Explorer no espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-115">As you are preparing and planning your MED-V deployment, you will have to identify and compile a list of the URL addresses to redirect from Internet Explorer on the host computer to Internet Explorer in the MED-V workspace.</span></span>

<span data-ttu-id="1cd83-116">Por fim, avalie os requisitos de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="1cd83-116">Finally, you have to evaluate your disk space requirements.</span></span> <span data-ttu-id="1cd83-117">A maioria dos espaços de trabalho do MED-V tem 2 gigabytes (GB) ou mais.</span><span class="sxs-lookup"><span data-stu-id="1cd83-117">Most MED-V workspaces are 2 gigabytes (GB) or larger.</span></span> <span data-ttu-id="1cd83-118">O espaço disponível em disco em um sistema pode ser resumido rapidamente, dependendo do número de usuários e a configuração do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-118">The available disk space on a system can be consumed quickly, depending on the number of users and the configuration of MED-V.</span></span> <span data-ttu-id="1cd83-119">Além disso, o método de distribuição preferido da sua empresa pode exigir espaço adicional.</span><span class="sxs-lookup"><span data-stu-id="1cd83-119">Also, your company’s preferred method of distribution can require additional space.</span></span> <span data-ttu-id="1cd83-120">Geralmente, você deve liberar um mínimo de 10 GB de espaço em disco para um espaço de trabalho do MED-V, mas isso varia muito, dependendo do tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="1cd83-120">Generally, you should free a minimum of 10 GB of disk space for a MED-V workspace, but this varies greatly, depending on the size of the image.</span></span>

### <span data-ttu-id="1cd83-121">Calcular os requisitos de espaço em disco para os espaços de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="1cd83-121">Calculate the Disk Space Requirements for MED-V Workspaces</span></span>

<span data-ttu-id="1cd83-122">Um espaço de trabalho do MED-V requer memória e espaço em disco do computador host no qual ele está instalado.</span><span class="sxs-lookup"><span data-stu-id="1cd83-122">A MED-V workspace requires memory and disk space from the host computer on which it is installed.</span></span> <span data-ttu-id="1cd83-123">É preciso ter no mínimo 2 GB de espaço em disco no host.</span><span class="sxs-lookup"><span data-stu-id="1cd83-123">At a minimum, 2 GB of disk space are required on the host.</span></span> <span data-ttu-id="1cd83-124">O espaço em disco é variável e depende do número de aplicativos e dos dados em um espaço de trabalho do MED-V do usuário.</span><span class="sxs-lookup"><span data-stu-id="1cd83-124">Disk space is variable and depends on the number of applications and the data in a user’s MED-V workspace.</span></span>

<span data-ttu-id="1cd83-125">Recomendamos um mínimo de 10 GB de espaço em disco para o MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-125">We recommend a minimum of 10 GB of disk space for MED-V.</span></span> <span data-ttu-id="1cd83-126">Esse valor permite um espaço de trabalho básico do Windows XP e alguns aplicativos e redirecionamento de Web instalados.</span><span class="sxs-lookup"><span data-stu-id="1cd83-126">This amount allows for a basic Windows XP workspace and some basic installed applications and web redirection.</span></span> <span data-ttu-id="1cd83-127">Ele também fornece espaço disponível para a unidade de troca de host.</span><span class="sxs-lookup"><span data-stu-id="1cd83-127">It also provides available space for the host swap drive.</span></span> <span data-ttu-id="1cd83-128">Em uma configuração básica, o MED-V e um único espaço de trabalho do MED-V implantado consomem até 6 a 8 GB.</span><span class="sxs-lookup"><span data-stu-id="1cd83-128">In a basic configuration, MED-V and a single deployed MED-V workspace consume as much as 6 to 8 GB.</span></span> <span data-ttu-id="1cd83-129">Se você incluir muitos aplicativos no espaço de trabalho do MED-V ou tiver mais de um usuário por computador, poderá usar o seguinte cálculo para determinar o espaço em disco que o seu espaço de trabalho do MED-V requer:</span><span class="sxs-lookup"><span data-stu-id="1cd83-129">If you include lots of applications on the MED-V workspace or have more than one user per computer, then you can use the following calculation to more accurately determine the disk space your MED-V workspace requires:</span></span>

*<span data-ttu-id="1cd83-130">VHD + base (usuário por computador x (disco de diferença + estado salvo))</span><span class="sxs-lookup"><span data-stu-id="1cd83-130">Base VHD + (User per computer x (Difference Disk + Saved State))</span></span>*

<span data-ttu-id="1cd83-131">Para calcular o espaço em disco necessário, determine o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1cd83-131">To calculate the required disk space, determine the following:</span></span>

-   <span data-ttu-id="1cd83-132">**Tamanho do VHD base** – o disco rígido virtual que foi usado para criar o espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-132">**Size of the base VHD** – the virtual hard disk that was used to create the MED-V workspace.</span></span>

    <span data-ttu-id="1cd83-133">**Importante**  Não use o tamanho do arquivo. medv para o seu cálculo porque o arquivo. medv está compactado.</span><span class="sxs-lookup"><span data-stu-id="1cd83-133">**Important** Do not use the .medv file size for your calculation because the .medv file is compressed.</span></span>

     

-   <span data-ttu-id="1cd83-134">**Usuários por computador** – med-v cria um espaço de trabalho do MED-v para cada usuário em um computador; o espaço de trabalho do MED-V consome espaço em disco quando cada usuário se conecta e o espaço de trabalho do MED-V é criado.</span><span class="sxs-lookup"><span data-stu-id="1cd83-134">**Users per computer** – MED-V creates a MED-V workspace for each user on a computer; the MED-V workspace consumes disk space as each user logs on and the MED-V workspace is created.</span></span>

-   <span data-ttu-id="1cd83-135">**Tamanho do disco diferencial** – usado para acompanhar a diferença do VHD base.</span><span class="sxs-lookup"><span data-stu-id="1cd83-135">**Size of the differencing disk** – used to track the difference from the base VHD.</span></span> <span data-ttu-id="1cd83-136">Esse tamanho varia à medida que você adiciona aplicativos e atualizações de software ao disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="1cd83-136">This size varies as you add applications and software updates to the virtual hard disk.</span></span> <span data-ttu-id="1cd83-137">Um disco diferencial é criado para cada usuário do MED-V quando eles iniciam MED-V pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="1cd83-137">A differencing disk is created for each MED-V user when they start MED-V for the first time.</span></span>

-   <span data-ttu-id="1cd83-138">**Tamanho do arquivo de estado salvo** – usado para manter o estado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cd83-138">**Size of the Saved State file** – used to maintain state in the virtual machine.</span></span> <span data-ttu-id="1cd83-139">Geralmente, isso é um pouco maior do que a RAM alocada para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1cd83-139">Typically, this is just a bit larger than the allocated RAM for the virtual machine.</span></span> <span data-ttu-id="1cd83-140">Por exemplo, 1 GB de RAM alocado cria um arquivo sobre 1.081.000 KB.</span><span class="sxs-lookup"><span data-stu-id="1cd83-140">For example, 1 GB of RAM allocated creates a file about 1,081,000 KB.</span></span>

<span data-ttu-id="1cd83-141">O exemplo a seguir mostra um cálculo com base em três usuários de um espaço de trabalho do MED-V que tem um disco rígido virtual de 2,6 GB:</span><span class="sxs-lookup"><span data-stu-id="1cd83-141">The following example shows a calculation based on three users of a MED-V workspace that has a 2.6 GB virtual hard disk:</span></span>

*<span data-ttu-id="1cd83-142">2.6 GB + (3 x (1,5 GB + 1GB)) = 10.1 GB</span><span class="sxs-lookup"><span data-stu-id="1cd83-142">2.6gb + (3 x (1.5gb + 1gb)) = 10.1gb</span></span>*

<span data-ttu-id="1cd83-143">**Observação**  Uma prática recomendada do MED-V é calcular o espaço necessário usando uma implantação de laboratório para validar os requisitos.</span><span class="sxs-lookup"><span data-stu-id="1cd83-143">**Note** A MED-V best practice is to calculate the required space by using a lab deployment to validate the requirements.</span></span>

 

### <span data-ttu-id="1cd83-144">Localizar os arquivos para determinar o tamanho do arquivo</span><span class="sxs-lookup"><span data-stu-id="1cd83-144">Locate the Files to Determine File Size</span></span>

<span data-ttu-id="1cd83-145">Os seguintes locais contêm os arquivos para as configurações do computador e do usuário:</span><span class="sxs-lookup"><span data-stu-id="1cd83-145">The following locations contain the files for the computer and user settings:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1cd83-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="1cd83-146">Type</span></span></th>
<th align="left"><span data-ttu-id="1cd83-147">Localização</span><span class="sxs-lookup"><span data-stu-id="1cd83-147">Location</span></span></th>
<th align="left"><span data-ttu-id="1cd83-148">Arquivos</span><span class="sxs-lookup"><span data-stu-id="1cd83-148">Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cd83-149">VHD base</span><span class="sxs-lookup"><span data-stu-id="1cd83-149">Base VHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cd83-150">%ProgramData%\Microsoft\Medv\Workspace</span><span class="sxs-lookup"><span data-stu-id="1cd83-150">%ProgramData%\Microsoft\Medv\Workspace</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="1cd83-151">InternalName </em> . vhd-Where <em> InternalName </em> é o nome do disco rígido virtual selecionado no pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cd83-151">InternalName</em>.vhd - Where <em>InternalName</em> is the name of the virtual hard disk that you selected in the MED-V Workspace Packager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1cd83-152">Disco diferencial</span><span class="sxs-lookup"><span data-stu-id="1cd83-152">Differencing Disk</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cd83-153">Máquinas%LocalAppData%\Microsoft\MEDV\v2\Virtual</span><span class="sxs-lookup"><span data-stu-id="1cd83-153">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="1cd83-154">WorkspaceName </em> . vhd</span><span class="sxs-lookup"><span data-stu-id="1cd83-154">WorkspaceName</em>.vhd</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1cd83-155">Arquivo de estado salvo</span><span class="sxs-lookup"><span data-stu-id="1cd83-155">Saved State File</span></span></p></td>
<td align="left"><p><span data-ttu-id="1cd83-156">Máquinas%LocalAppData%\Microsoft\MEDV\v2\Virtual</span><span class="sxs-lookup"><span data-stu-id="1cd83-156">%LocalAppData%\Microsoft\MEDV\v2\Virtual Machines</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="1cd83-157">WorkspaceName </em> . VSV</span><span class="sxs-lookup"><span data-stu-id="1cd83-157">WorkspaceName</em>.vsv</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="1cd83-158">Calcular os requisitos de espaço em disco para espaços de trabalho do MED-V compartilhados</span><span class="sxs-lookup"><span data-stu-id="1cd83-158">Calculate the Disk Space Requirements for Shared MED-V Workspaces</span></span>

<span data-ttu-id="1cd83-159">Se você estiver calculando uma implantação do espaço de trabalho do MED-V compartilhado em um único computador, o número de usuários por computador em seu cálculo será sempre "1" porque o MED-V configura apenas um único disco diferencial para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="1cd83-159">If you are calculating for a shared MED-V workspace deployment on a single computer, then the number of users per computer in your calculation is always “1” because MED-V only configures a single differencing disk for all users.</span></span>

<span data-ttu-id="1cd83-160">Você pode encontrar o disco diferencial e o arquivo de estado salvo para os espaços de trabalho do MED-V compartilhados no%ProgramData%\\Microsoft\\Medv\\AllUsers.</span><span class="sxs-lookup"><span data-stu-id="1cd83-160">You can find the differencing disk and the saved state file for shared MED-V workspaces in %ProgramData%\\Microsoft\\Medv\\AllUsers.</span></span>

## <span data-ttu-id="1cd83-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1cd83-161">Related topics</span></span>


[<span data-ttu-id="1cd83-162">Definir e planejar sua implantação da MED-V</span><span class="sxs-lookup"><span data-stu-id="1cd83-162">Define and Plan your MED-V Deployment</span></span>](define-and-plan-your-med-v-deployment.md)

[<span data-ttu-id="1cd83-163">Planejamento para o MED-V</span><span class="sxs-lookup"><span data-stu-id="1cd83-163">Planning for MED-V</span></span>](planning-for-med-v.md)

 

 





