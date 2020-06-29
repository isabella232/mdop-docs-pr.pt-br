---
title: Como empacotar uma imagem do MED-V
description: Como empacotar uma imagem do MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799520"
---
# <span data-ttu-id="9aa4f-103">Como empacotar uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="9aa4f-103">How to Pack a MED-V Image</span></span>


<span data-ttu-id="9aa4f-104">Uma imagem do MED-V deve ser empacotada antes de poder ser adicionada a um pacote de implantação ou carregada no servidor.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-104">A MED-V image must be packed before it can be added to a deployment package or uploaded to the server.</span></span>

**<span data-ttu-id="9aa4f-105">Para criar uma imagem do MED-V compactada</span><span class="sxs-lookup"><span data-stu-id="9aa4f-105">To create a packed MED-V image</span></span>**

1.  <span data-ttu-id="9aa4f-106">Clique no botão gerenciamento de **imagens** .</span><span class="sxs-lookup"><span data-stu-id="9aa4f-106">Click the **Images** management button.</span></span>

2.  <span data-ttu-id="9aa4f-107">No módulo **imagens** , no painel **imagens compactadas locais** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-107">In the **Images** module, in the **Local Packed Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="9aa4f-108">Na caixa de diálogo **criação de imagem empacotada** , selecione a imagem da máquina virtual seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="9aa4f-108">In the **Packed Image Creation** dialog box, select the virtual machine image by doing one of the following:</span></span>

    -   <span data-ttu-id="9aa4f-109">No campo **base do arquivo de imagem** , digite o caminho completo do diretório em que a imagem do Microsoft Virtual PC preparado para o MED-V está localizada.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-109">In the **Base image file** field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="9aa4f-110">Clique em **procurar** para navegar até o diretório onde a imagem do Microsoft Virtual PC preparado para o MED-V está localizada.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-110">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="9aa4f-111">Especifique o nome da nova imagem seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="9aa4f-111">Specify the name of the new image by doing one of the following:</span></span>

    -   <span data-ttu-id="9aa4f-112">No campo **nome da imagem** , digite o nome desejado.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-112">In the **Image name** field, type the desired name.</span></span>

        **<span data-ttu-id="9aa4f-113">Observação</span><span class="sxs-lookup"><span data-stu-id="9aa4f-113">Note</span></span>**  
        <span data-ttu-id="9aa4f-114">Os seguintes caracteres não podem ser incluídos no nome da imagem: espaço " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="9aa4f-114">The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. <span data-ttu-id="9aa4f-115">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-115">Click **OK**.</span></span>

   <span data-ttu-id="9aa4f-116">Uma nova imagem empacotada do MED-V é criada em seu computador host com as propriedades definidas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-116">A new MED-V packed image is created on your host computer with the properties defined in the following table.</span></span>

**<span data-ttu-id="9aa4f-117">Observação</span><span class="sxs-lookup"><span data-stu-id="9aa4f-117">Note</span></span>**  
<span data-ttu-id="9aa4f-118">Nas **imagens compactadas locais** e **imagens compactadas nos** painéis do servidor, a versão mais recente de cada imagem é exibida como o nó pai.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-118">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="9aa4f-119">Clique no nó pai para ver todas as outras versões existentes da imagem.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-119">Click the parent node to view all other existing versions of the image.</span></span>



**<span data-ttu-id="9aa4f-120">Propriedades de imagens compactadas locais</span><span class="sxs-lookup"><span data-stu-id="9aa4f-120">Local Packed Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9aa4f-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9aa4f-121">Property</span></span></th>
<th align="left"><span data-ttu-id="9aa4f-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="9aa4f-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9aa4f-123">Nome da imagem</span><span class="sxs-lookup"><span data-stu-id="9aa4f-123">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="9aa4f-124">O nome da imagem empacotada conforme definido quando o administrador criou a imagem.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-124">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9aa4f-125">Versão</span><span class="sxs-lookup"><span data-stu-id="9aa4f-125">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="9aa4f-126">A versão da imagem exibida.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-126">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="9aa4f-127">Observação</span><span class="sxs-lookup"><span data-stu-id="9aa4f-127">Note</span></span></strong><br/><p><span data-ttu-id="9aa4f-128">Todas as versões anteriores são mantidas, a menos que sejam excluídas.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-128">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9aa4f-129">Tamanho do arquivo (compactado)</span><span class="sxs-lookup"><span data-stu-id="9aa4f-129">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9aa4f-130">O tamanho compactado físico da imagem.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-130">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9aa4f-131">Tamanho da imagem (não compactado)</span><span class="sxs-lookup"><span data-stu-id="9aa4f-131">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="9aa4f-132">O tamanho físico não compactado da imagem.</span><span class="sxs-lookup"><span data-stu-id="9aa4f-132">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9aa4f-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9aa4f-133">Related topics</span></span>


[<span data-ttu-id="9aa4f-134">Como instalar o cliente MED-V e o Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="9aa4f-134">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="9aa4f-135">Usando a interface de usuário do Console de Gerenciamento do MED-V</span><span class="sxs-lookup"><span data-stu-id="9aa4f-135">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="9aa4f-136">Criando uma imagem do Virtual PC para o MED-V</span><span class="sxs-lookup"><span data-stu-id="9aa4f-136">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)









