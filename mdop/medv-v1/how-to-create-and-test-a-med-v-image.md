---
title: Como criar e testar uma imagem do MED-V
description: Como criar e testar uma imagem do MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799993"
---
# <span data-ttu-id="47653-103">Como criar e testar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-103">How to Create and Test a MED-V Image</span></span>


<span data-ttu-id="47653-104">O administrador do MED-V cria uma imagem do MED-V para que possa ser carregada, associada a um espaço de trabalho do MED-V e, em seguida, distribuída para o cliente pela Web, adicionada a um pacote do MED-V ou baixada para o cliente usando um sistema de terceiros.</span><span class="sxs-lookup"><span data-stu-id="47653-104">The MED-V administrator creates a MED-V image so that it can be uploaded, associated with a MED-V workspace, and then distributed to the client over the Web, added to a MED-V package, or downloaded to the client by using a third-party system.</span></span> <span data-ttu-id="47653-105">É recomendável primeiro criar uma imagem de teste e testá-la no cliente MED-V antes de implantá-la.</span><span class="sxs-lookup"><span data-stu-id="47653-105">It is recommended to first create a test image and test it on MED-V client before deploying it.</span></span>

<span data-ttu-id="47653-106">Ao criar uma imagem do MED-V, ela passa pelos seguintes estágios:</span><span class="sxs-lookup"><span data-stu-id="47653-106">When creating a MED-V image, it goes through the following stages:</span></span>

1.  <span data-ttu-id="47653-107">**Imagem de teste local**— uma imagem básica que pode ser testada localmente.</span><span class="sxs-lookup"><span data-stu-id="47653-107">**Local test image**—A basic image that can be tested locally.</span></span>

2.  <span data-ttu-id="47653-108">**Imagem empacotada local**– após a imagem ser testada, a imagem é compactada como era antes do teste.</span><span class="sxs-lookup"><span data-stu-id="47653-108">**Local packed image**—After the image is tested, the image is packed as it existed prior to testing.</span></span> <span data-ttu-id="47653-109">Nenhuma alteração feita durante o teste está incluída na imagem empacotada.</span><span class="sxs-lookup"><span data-stu-id="47653-109">No changes made during testing are included in the packed image.</span></span>

3.  <span data-ttu-id="47653-110">**Imagem empacotada no servidor**— a imagem empacotada é carregada no servidor.</span><span class="sxs-lookup"><span data-stu-id="47653-110">**Packed image on server**—The packed image is uploaded to the server.</span></span>

## <span data-ttu-id="47653-111">Como criar uma imagem de teste do MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-111">How to Create a MED-V Test Image</span></span>


**<span data-ttu-id="47653-112">Para criar uma nova imagem de teste do MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-112">To create a new MED-V test image</span></span>**

1.  <span data-ttu-id="47653-113">Clique no botão gerenciamento de **imagens** .</span><span class="sxs-lookup"><span data-stu-id="47653-113">Click the **Images** management button.</span></span>

    <span data-ttu-id="47653-114">O módulo **imagens** é exibido.</span><span class="sxs-lookup"><span data-stu-id="47653-114">The **Images** module appears.</span></span>

    -   <span data-ttu-id="47653-115">O módulo **imagens** consiste nos seguintes painéis:</span><span class="sxs-lookup"><span data-stu-id="47653-115">The **Images** module consists of the following panes:</span></span>

        -   <span data-ttu-id="47653-116">**Imagens de teste locais**— imagens descompactadas locais.</span><span class="sxs-lookup"><span data-stu-id="47653-116">**Local Test Images**—Local unpacked images.</span></span>

        -   <span data-ttu-id="47653-117">**Imagens compactadas locais**– todas as imagens compactadas no computador local.</span><span class="sxs-lookup"><span data-stu-id="47653-117">**Local Packed Images**—All packed images on the local computer.</span></span>

        -   <span data-ttu-id="47653-118">**Imagens compactadas no servidor**— todas as imagens que foram empacotadas e carregadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="47653-118">**Packed Images on Server**—All images that have been packed and uploaded to the server.</span></span>

    -   <span data-ttu-id="47653-119">Nas **imagens compactadas locais** e **imagens compactadas nos** painéis do servidor, a versão mais recente de cada imagem é exibida como o nó pai.</span><span class="sxs-lookup"><span data-stu-id="47653-119">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="47653-120">Clique no nó pai para ver todas as outras versões existentes da imagem.</span><span class="sxs-lookup"><span data-stu-id="47653-120">Click the parent node to view all other existing versions of the image.</span></span>

2.  <span data-ttu-id="47653-121">No painel **imagens de teste locais** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="47653-121">In the **Local Test Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="47653-122">Na caixa de diálogo **testar criação de imagem** , selecione a imagem da máquina virtual que você deseja configurar como uma imagem de teste do MED-V seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="47653-122">On the **Test Image Creation** dialog box, select the virtual machine image that you want to configure as a MED-V test image by doing one of the following:</span></span>

    -   <span data-ttu-id="47653-123">No campo **base** do arquivo de imagem, digite o caminho completo do diretório em que a imagem do Microsoft Virtual PC preparado para o MED-V está localizada.</span><span class="sxs-lookup"><span data-stu-id="47653-123">In the **Base image** file field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="47653-124">Clique em **procurar** para navegar até o diretório onde a imagem do Microsoft Virtual PC preparado para o MED-V está localizada.</span><span class="sxs-lookup"><span data-stu-id="47653-124">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="47653-125">No campo **nome da imagem** , digite ou selecione o nome desejado.</span><span class="sxs-lookup"><span data-stu-id="47653-125">In the **Image name** field, type or select the desired name.</span></span>

    <span data-ttu-id="47653-126">**Observação**  Os seguintes caracteres não podem ser incluídos no nome da imagem: espaço " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="47653-126">**Note** The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>

     

5.  <span data-ttu-id="47653-127">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="47653-127">Click **OK**.</span></span>

    <span data-ttu-id="47653-128">Uma nova imagem de teste do MED-V é criada no computador host com as propriedades definidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="47653-128">A new MED-V test image is created on your host computer with the properties defined in the following table.</span></span>

    <span data-ttu-id="47653-129">Para obter mais informações sobre como configurar a imagem do espaço de trabalho do MED-V, consulte [Configurando políticas do espaço de trabalho do MED-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="47653-129">For more information about configuring the MED-V workspace image, refer to [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

**<span data-ttu-id="47653-130">Propriedades de imagens de teste locais</span><span class="sxs-lookup"><span data-stu-id="47653-130">Local Test Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="47653-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="47653-131">Property</span></span></th>
<th align="left"><span data-ttu-id="47653-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="47653-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47653-133">Nome da imagem</span><span class="sxs-lookup"><span data-stu-id="47653-133">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="47653-134">O nome da imagem de teste conforme definido quando o administrador criou a imagem.</span><span class="sxs-lookup"><span data-stu-id="47653-134">The name of the test image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="47653-135">Caminho da imagem</span><span class="sxs-lookup"><span data-stu-id="47653-135">Image Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="47653-136">O caminho local da imagem de teste.</span><span class="sxs-lookup"><span data-stu-id="47653-136">The local path of the test image.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="47653-137">Criado</span><span class="sxs-lookup"><span data-stu-id="47653-137">Created</span></span></p></td>
<td align="left"><p><span data-ttu-id="47653-138">A data em que a imagem de teste foi criada.</span><span class="sxs-lookup"><span data-stu-id="47653-138">The date the test image was created.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="47653-139">Como testar uma imagem do MED-V do cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-139">How to Test a MED-V Image from the MED-V Client</span></span>


<span data-ttu-id="47653-140">Após a criação de uma imagem de teste do MED-V, use o procedimento a seguir para testar a imagem localmente.</span><span class="sxs-lookup"><span data-stu-id="47653-140">After a MED-V test image is created, use the following procedure to test the image locally.</span></span>

**<span data-ttu-id="47653-141">Para testar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-141">To test a MED-V image</span></span>**

1.  <span data-ttu-id="47653-142">Clique no botão gerenciamento de **políticas** .</span><span class="sxs-lookup"><span data-stu-id="47653-142">Click the **Policy** management button.</span></span>

2.  <span data-ttu-id="47653-143">No módulo de **política** , atribua a imagem de teste do MED-v a um espaço de trabalho do MED-v fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="47653-143">In the **Policy** module, assign the MED-V test image to a MED-V workspace by doing the following:</span></span>

    1.  <span data-ttu-id="47653-144">Clique na guia **máquina virtual** .</span><span class="sxs-lookup"><span data-stu-id="47653-144">Click the **Virtual Machine** tab.</span></span>

    2.  <span data-ttu-id="47653-145">No campo de **imagem atribuído** , selecione a imagem de teste do MED-V que você criou.</span><span class="sxs-lookup"><span data-stu-id="47653-145">In the **Assigned Image** field, select the MED-V test image you created.</span></span> <span data-ttu-id="47653-146">Se a sua imagem de teste não estiver na lista, clique em **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="47653-146">If your test image is not in the list, click **Refresh**.</span></span>

    3.  <span data-ttu-id="47653-147">Na barra de ferramentas, clique em **salvar alterações**.</span><span class="sxs-lookup"><span data-stu-id="47653-147">On the toolbar, click **Save changes**.</span></span>

3.  <span data-ttu-id="47653-148">Configure qualquer outra configuração de espaço de trabalho do MED-V para ser testada.</span><span class="sxs-lookup"><span data-stu-id="47653-148">Configure any other MED-V workspace settings to be tested.</span></span> <span data-ttu-id="47653-149">Para obter mais informações, consulte [Configurando políticas do espaço de trabalho do MED-V](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="47653-149">For more information, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

4.  <span data-ttu-id="47653-150">Inicie o cliente MED-V.</span><span class="sxs-lookup"><span data-stu-id="47653-150">Start MED-V client.</span></span>

5.  <span data-ttu-id="47653-151">Na caixa de confirmação **confirmar teste em execução** , clique em **usar imagem de teste**.</span><span class="sxs-lookup"><span data-stu-id="47653-151">In the **Confirm Running Test** confirmation box, click **Use Test Image**.</span></span>

6.  <span data-ttu-id="47653-152">Testar a imagem de teste do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="47653-152">Test the MED-V workspace test image.</span></span>

    <span data-ttu-id="47653-153">Para obter informações sobre como iniciar e executar o cliente MED-V, consulte [operações do cliente med-v](med-v-client-operations.md).</span><span class="sxs-lookup"><span data-stu-id="47653-153">For information about starting and running MED-V client, see [MED-V Client Operations](med-v-client-operations.md).</span></span>

<span data-ttu-id="47653-154">**Observação**  Ao testar uma imagem, não abra o VPC e faça alterações na imagem.</span><span class="sxs-lookup"><span data-stu-id="47653-154">**Note** While testing an image, do not open VPC and make changes to the image.</span></span>

 

<span data-ttu-id="47653-155">**Observação**  Ao testar uma imagem, nenhuma alteração é salva na imagem entre as sessões; em vez disso, eles são salvos em um arquivo separado temporário.</span><span class="sxs-lookup"><span data-stu-id="47653-155">**Note** When testing an image, no changes are saved to the image between sessions; instead, they are saved in a separate, temporary file.</span></span> <span data-ttu-id="47653-156">Isso é para garantir que, quando a imagem é empacotada e executada no ambiente de produção, seja a imagem original e limpa.</span><span class="sxs-lookup"><span data-stu-id="47653-156">This is to ensure that when the image is packed and run on the production environment, it is the original, clean image.</span></span>

 

## <span data-ttu-id="47653-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47653-157">Related topics</span></span>


[<span data-ttu-id="47653-158">Criando uma imagem do Virtual PC para o MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-158">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="47653-159">Criando um espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-159">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="47653-160">Configurando políticas de espaço de trabalho do MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-160">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="47653-161">Operações do cliente MED-V</span><span class="sxs-lookup"><span data-stu-id="47653-161">MED-V Client Operations</span></span>](med-v-client-operations.md)

 

 





