---
title: Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação
description: Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação
author: dansimp
ms.assetid: 07c5d539-51d9-4759-adc7-72b40d5d7bb3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e3647d684f64a0635e2875314498bde841204369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799461"
---
# <span data-ttu-id="3674e-103">Como implantar a imagem de recuperação do DaRT como parte de uma partição de recuperação</span><span class="sxs-lookup"><span data-stu-id="3674e-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="3674e-104">Após concluir a execução do assistente de imagem de recuperação do Microsoft diagnóstico e recuperação (DaRT) 8,0 e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição de recuperação em uma imagem do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3674e-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 8 image.</span></span> <span data-ttu-id="3674e-105">Uma partição é recomendada, porque qualquer problema de corrupção que impede o sistema operacional Windows de iniciar também impediria que a imagem de recuperação seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="3674e-105">A partition is recommended, because any corruption issues that prevent the Windows operating system from starting would also prevent the recovery image from starting.</span></span> <span data-ttu-id="3674e-106">Uma partição separada também elimina a necessidade de fornecer a chave de recuperação do BitLocker duas vezes.</span><span class="sxs-lookup"><span data-stu-id="3674e-106">A separate partition also eliminates the need to provide the BitLocker recovery key twice.</span></span> <span data-ttu-id="3674e-107">Considere ocultar a partição para impedir que os usuários armazenem arquivos nela.</span><span class="sxs-lookup"><span data-stu-id="3674e-107">Consider hiding the partition to prevent users from storing files on it.</span></span>

**<span data-ttu-id="3674e-108">Para implantar o DaRT na partição de recuperação de uma imagem do Windows 8</span><span class="sxs-lookup"><span data-stu-id="3674e-108">To deploy DaRT in the recovery partition of a Windows 8 image</span></span>**

1.  <span data-ttu-id="3674e-109">Crie uma partição de destino na sua imagem do Windows 8 que seja igual ou superior ao tamanho do arquivo de imagem ISO que você criou usando o **Assistente de imagem de recuperação DaRT 8,0**.</span><span class="sxs-lookup"><span data-stu-id="3674e-109">Create a target partition in your Windows 8 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT 8.0 Recovery Image wizard**.</span></span>

    <span data-ttu-id="3674e-110">O tamanho mínimo necessário para uma partição DaRT é 500MB para acomodar a funcionalidade de conexão remota no DaRT.</span><span class="sxs-lookup"><span data-stu-id="3674e-110">The minimum size required for a DaRT partition is 500MB to accommodate the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="3674e-111">Extraia o arquivo boot. wim do arquivo de imagem ISO do DaRT.</span><span class="sxs-lookup"><span data-stu-id="3674e-111">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="3674e-112">Usando o método preferido da sua empresa, monte o arquivo de imagem ISO que você criou na página **criar imagem de inicialização** .</span><span class="sxs-lookup"><span data-stu-id="3674e-112">Using your company’s preferred method, mount the ISO image file that you created on the **Create Startup Image** page.</span></span>

    2.  <span data-ttu-id="3674e-113">Abra o arquivo de imagem ISO e copie o arquivo boot. wim da pasta \\sources na imagem montada para um local no seu computador ou em uma unidade externa.</span><span class="sxs-lookup"><span data-stu-id="3674e-113">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="3674e-114">**Observação**  Se você gravou um CD, DVD ou USB da imagem de recuperação, poderá abrir os arquivos na mídia removível e copiar o arquivo boot. wim da pasta \\sources.</span><span class="sxs-lookup"><span data-stu-id="3674e-114">**Note** If you burned a CD, DVD, or USB of the recovery image, you can open the files on the removable media and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="3674e-115">Se você copiar um arquivo boot. wim, não será necessário montar a imagem.</span><span class="sxs-lookup"><span data-stu-id="3674e-115">If you copy boot.wim file, you don’t need to mount the image.</span></span>

         

3.  <span data-ttu-id="3674e-116">Use o arquivo boot. wim para criar uma partição de recuperação inicializável usando o método padrão de sua empresa para criar uma imagem personalizada do Windows RE.</span><span class="sxs-lookup"><span data-stu-id="3674e-116">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="3674e-117">Para obter mais informações sobre como criar ou personalizar uma partição de recuperação, consulte [Personalizando a experiência do Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="3674e-117">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="3674e-118">Substitua a partição de destino na sua imagem do Windows 8 pela partição de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3674e-118">Replace the target partition in your Windows 8 image with the recovery partition.</span></span>

    <span data-ttu-id="3674e-119">Para obter mais informações sobre como implantar uma solução de recuperação para reinstalar a imagem de fábrica em caso de falha do sistema, consulte [implantar uma imagem de recuperação do sistema](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="3674e-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="3674e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3674e-120">Related topics</span></span>


[<span data-ttu-id="3674e-121">Criação da imagem de recuperação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="3674e-121">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="3674e-122">Implantação da imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="3674e-122">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="3674e-123">Planejamento para o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="3674e-123">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 





