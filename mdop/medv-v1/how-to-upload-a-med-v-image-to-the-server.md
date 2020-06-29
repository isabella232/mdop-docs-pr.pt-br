---
title: Como carregar uma imagem do MED-V no servidor
description: Como carregar uma imagem do MED-V no servidor
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799725"
---
# <span data-ttu-id="4fcdb-103">Como carregar uma imagem do MED-V no servidor</span><span class="sxs-lookup"><span data-stu-id="4fcdb-103">How to Upload a MED-V Image to the Server</span></span>


<span data-ttu-id="4fcdb-104">Depois que uma imagem do MED-V tiver sido testada, ela poderá ser empacotada e, em seguida, carregada para o servidor.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-104">After a MED-V image has been tested, it can be packed and then uploaded to the server.</span></span> <span data-ttu-id="4fcdb-105">Para obter informações sobre como configurar um servidor de distribuição da Web Image, consulte [como configurar o servidor de distribuição da Web de imagem](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="4fcdb-105">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span>

<span data-ttu-id="4fcdb-106">Depois que uma imagem do MED-V é compactada e carregada no servidor, ela pode ser distribuída aos usuários usando um centro de distribuição de software corporativo ou pode ser baixada pelos usuários que usam um pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-106">Once a MED-V image is packed and uploaded to the server, it can be distributed to users by using an enterprise software distribution center, or it can be downloaded by users using a deployment package.</span></span> <span data-ttu-id="4fcdb-107">Para obter informações sobre a implantação usando um centro de distribuição de software corporativo, consulte [implantando um espaço de trabalho do MED-V usando um sistema de distribuição de software corporativo](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="4fcdb-107">For information on deployment using an enterprise software distribution center, see [Deploying a MED-V Workspace Using an Enterprise Software Distribution System](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span></span> <span data-ttu-id="4fcdb-108">Para obter informações sobre a implantação usando um pacote, consulte [implantando um espaço de trabalho do MED-V usando um pacote de implantação](deploying-a-med-v-workspace-using-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="4fcdb-108">For information on deployment using a package, see [Deploying a MED-V Workspace Using a Deployment Package](deploying-a-med-v-workspace-using-a-deployment-package.md).</span></span>

**<span data-ttu-id="4fcdb-109">Observação</span><span class="sxs-lookup"><span data-stu-id="4fcdb-109">Note</span></span>**  
<span data-ttu-id="4fcdb-110">Antes de carregar uma imagem, verifique se um proxy da Web não está definido nas configurações do navegador e se o Windows Update não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-110">Before uploading an image, verify that a Web proxy is not defined in your browser settings and that Windows Update is not currently running.</span></span>



**<span data-ttu-id="4fcdb-111">Para carregar uma imagem do MED-V para o servidor</span><span class="sxs-lookup"><span data-stu-id="4fcdb-111">To upload a MED-V image to the server</span></span>**

1.  <span data-ttu-id="4fcdb-112">No painel **imagens compactadas locais** , selecione a imagem que você criou.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-112">In the **Local Packed Images** pane, select the image you created.</span></span>

2.  <span data-ttu-id="4fcdb-113">Clique em **carregar**.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-113">Click **Upload**.</span></span>

    <span data-ttu-id="4fcdb-114">A imagem é carregada no servidor.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-114">The image is uploaded to the server.</span></span> <span data-ttu-id="4fcdb-115">Isso pode demorar um pouco.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-115">This might take a considerable amount of time.</span></span>

    <span data-ttu-id="4fcdb-116">As imagens no servidor são definidas com as propriedades listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-116">Images on the server are defined with the properties listed in the following table.</span></span>

**<span data-ttu-id="4fcdb-117">Imagens compactadas nas propriedades do servidor</span><span class="sxs-lookup"><span data-stu-id="4fcdb-117">Packed Images on Server Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4fcdb-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4fcdb-118">Property</span></span></th>
<th align="left"><span data-ttu-id="4fcdb-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="4fcdb-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4fcdb-120">Nome da imagem</span><span class="sxs-lookup"><span data-stu-id="4fcdb-120">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="4fcdb-121">O nome da imagem empacotada conforme definido quando o administrador criou a imagem.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-121">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4fcdb-122">Versão</span><span class="sxs-lookup"><span data-stu-id="4fcdb-122">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="4fcdb-123">A versão da imagem exibida.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-123">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="4fcdb-124">Observação</span><span class="sxs-lookup"><span data-stu-id="4fcdb-124">Note</span></span></strong><br/><p><span data-ttu-id="4fcdb-125">Todas as versões anteriores são mantidas, a menos que sejam excluídas.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-125">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4fcdb-126">Tamanho do arquivo (compactado)</span><span class="sxs-lookup"><span data-stu-id="4fcdb-126">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4fcdb-127">O tamanho compactado físico da imagem.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-127">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4fcdb-128">Tamanho da imagem (não compactado)</span><span class="sxs-lookup"><span data-stu-id="4fcdb-128">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="4fcdb-129">O tamanho físico não compactado da imagem.</span><span class="sxs-lookup"><span data-stu-id="4fcdb-129">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="4fcdb-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4fcdb-130">Related topics</span></span>


[<span data-ttu-id="4fcdb-131">Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="4fcdb-131">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="4fcdb-132">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="4fcdb-132">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="4fcdb-133">Criando uma imagem do Virtual PC para o MED-V</span><span class="sxs-lookup"><span data-stu-id="4fcdb-133">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="4fcdb-134">Como empacotar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="4fcdb-134">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)









