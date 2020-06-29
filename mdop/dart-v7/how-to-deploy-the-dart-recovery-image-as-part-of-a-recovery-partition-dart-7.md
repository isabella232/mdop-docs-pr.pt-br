---
title: Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação
description: Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799296"
---
# <span data-ttu-id="1ad1d-103">Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação</span><span class="sxs-lookup"><span data-stu-id="1ad1d-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="1ad1d-104">Depois de terminar de executar o assistente de recuperação de imagem do DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição de recuperação em uma imagem do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

**<span data-ttu-id="1ad1d-105">Para implantar o DaRT na partição de recuperação de uma imagem do Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ad1d-105">To deploy DaRT in the recovery partition of a Windows 7 image</span></span>**

1.  <span data-ttu-id="1ad1d-106">Crie uma partição de destino na sua imagem do Windows 7 que seja igual ou maior do que o tamanho do arquivo de imagem ISO que você criou usando o **Assistente de imagem de recuperação DART**.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-106">Create a target partition in your Windows 7 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT Recovery Image Wizard**.</span></span>

    <span data-ttu-id="1ad1d-107">O tamanho mínimo necessário para uma partição DaRT é de aproximadamente 300MB.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-107">The minimum size required for a DaRT partition is approximately 300MB.</span></span> <span data-ttu-id="1ad1d-108">No entanto, recomendamos que o 450MB acomode a funcionalidade de conexão remota no DaRT.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-108">However, we recommend 450MB to accommodate for the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="1ad1d-109">Extraia o arquivo boot. wim do arquivo de imagem ISO do DaRT.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-109">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="1ad1d-110">Monte o arquivo de imagem ISO que você criou na caixa de diálogo **criar imagem de inicialização** usando o método preferido da sua empresa para montar uma imagem.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-110">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="1ad1d-111">Abra o arquivo de imagem ISO e copie o arquivo boot. wim da pasta \\sources na imagem montada para um local no seu computador ou em uma unidade externa.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-111">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="1ad1d-112">**Observação**  Se você gravou um CD ou DVD da imagem de recuperação, poderá abrir os arquivos no CD ou DVD e copiar o arquivo boot. wim da pasta \\sources.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-112">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="1ad1d-113">Isso permite que você ignore a necessidade de montar a imagem.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-113">This lets you skip the need to mount the image.</span></span>

         

3.  <span data-ttu-id="1ad1d-114">Use o arquivo boot. wim para criar uma partição de recuperação inicializável usando o método padrão de sua empresa para criar uma imagem personalizada do Windows RE.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-114">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="1ad1d-115">Para obter mais informações sobre como criar ou personalizar uma partição de recuperação, consulte [Personalizando a experiência do Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="1ad1d-115">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="1ad1d-116">Substitua a partição de destino na sua imagem do Windows 7 pela partição de recuperação.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-116">Replace the target partition in your Windows 7 image with the recovery partition.</span></span>

<span data-ttu-id="1ad1d-117">Depois que a imagem do Windows 7 estiver pronta, distribua a imagem para os computadores da sua empresa usando o processo padrão de implantação de imagens da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-117">After your Windows 7 image is ready, distribute the image to computers in your enterprise by using your company’s standard image deployment process.</span></span> <span data-ttu-id="1ad1d-118">Para obter mais informações sobre como criar uma imagem do Windows 7, consulte [criando uma imagem padrão do Windows 7: guia](https://go.microsoft.com/fwlink/?LinkId=212103)passo a passo.</span><span class="sxs-lookup"><span data-stu-id="1ad1d-118">For more information about how to create a Windows 7 image, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=212103).</span></span>

<span data-ttu-id="1ad1d-119">Para obter mais informações sobre como implantar uma solução de recuperação para reinstalar a imagem de fábrica em caso de falha do sistema, consulte [implantar uma imagem de recuperação do sistema](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="1ad1d-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="1ad1d-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ad1d-120">Related topics</span></span>


[<span data-ttu-id="1ad1d-121">Implantação da imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="1ad1d-121">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





