---
title: Como implantar a imagem de recuperação do DaRT como uma partição remota
description: Como implantar a imagem de recuperação do DaRT como uma partição remota
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799298"
---
# <span data-ttu-id="c036c-103">Como implantar a imagem de recuperação do DaRT como uma partição remota</span><span class="sxs-lookup"><span data-stu-id="c036c-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="c036c-104">Depois de terminar de executar o assistente de imagem de recuperação DaRT e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição remota na rede.</span><span class="sxs-lookup"><span data-stu-id="c036c-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="c036c-105">Para implantar o DaRT como uma partição remota</span><span class="sxs-lookup"><span data-stu-id="c036c-105">To deploy DaRT as a remote partition</span></span>**

1.  <span data-ttu-id="c036c-106">Extraia o arquivo boot. wim do arquivo de imagem ISO do DaRT.</span><span class="sxs-lookup"><span data-stu-id="c036c-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="c036c-107">Monte o arquivo de imagem ISO que você criou na caixa de diálogo **criar imagem de inicialização** usando o método preferido da sua empresa para montar uma imagem.</span><span class="sxs-lookup"><span data-stu-id="c036c-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="c036c-108">Abra o arquivo de imagem ISO e copie o arquivo boot. wim da pasta \\sources na imagem montada para um local no seu computador ou em uma unidade externa.</span><span class="sxs-lookup"><span data-stu-id="c036c-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="c036c-109">**Observação**  Se você gravou um CD ou DVD da imagem de recuperação, poderá abrir os arquivos no CD ou DVD e copiar o arquivo boot. wim da pasta \\sources.</span><span class="sxs-lookup"><span data-stu-id="c036c-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="c036c-110">Isso permite que você ignore a necessidade de montar a imagem.</span><span class="sxs-lookup"><span data-stu-id="c036c-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="c036c-111">Implante o arquivo boot. wim em um servidor WDS que possa ser acessado dos computadores de usuários finais na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="c036c-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="c036c-112">Configure o servidor WDS para usar o arquivo boot. wim para DaRT seguindo seus procedimentos de implantação padrão do WDS.</span><span class="sxs-lookup"><span data-stu-id="c036c-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="c036c-113">Para obter mais informações sobre como implantar o DaRT como uma partição remota, consulte o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c036c-113">For more information about how to deploy DaRT as a remote partition, see the following:</span></span>

-   [<span data-ttu-id="c036c-114">Passo a passo: implantar uma imagem usando o PXE</span><span class="sxs-lookup"><span data-stu-id="c036c-114">Walkthrough: Deploy an Image by Using PXE</span></span>](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [<span data-ttu-id="c036c-115">Guia de introdução aos serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="c036c-115">Windows Deployment Services Getting Started Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=212106)

## <span data-ttu-id="c036c-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c036c-116">Related topics</span></span>


[<span data-ttu-id="c036c-117">Implantação da imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="c036c-117">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





