---
title: Como implantar a imagem de recuperação do DaRT como uma partição remota
description: Como implantar a imagem de recuperação do DaRT como uma partição remota
author: dansimp
ms.assetid: 58f4a6c6-6193-42bd-a095-0de868711af9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e9a6e3a9dc25139210ae22ba767da984e9a7b86d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797891"
---
# <span data-ttu-id="20a17-103">Como implantar a imagem de recuperação do DaRT como uma partição remota</span><span class="sxs-lookup"><span data-stu-id="20a17-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="20a17-104">Após concluir a execução do assistente de imagem de recuperação do Microsoft diagnóstico e recuperação (DaRT) 8,0 e criar a imagem de recuperação, você pode extrair o arquivo boot. wim do arquivo de imagem ISO e implantá-lo como uma partição remota na rede.</span><span class="sxs-lookup"><span data-stu-id="20a17-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="20a17-105">Para implantar o DaRT 8,0 como uma partição remota</span><span class="sxs-lookup"><span data-stu-id="20a17-105">To deploy DaRT 8.0 as a remote partition</span></span>**

1.  <span data-ttu-id="20a17-106">Extraia o arquivo boot. wim do arquivo de imagem ISO do DaRT.</span><span class="sxs-lookup"><span data-stu-id="20a17-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="20a17-107">Monte o arquivo de imagem ISO que você criou na caixa de diálogo **criar imagem de inicialização** usando o método preferido da sua empresa para montar uma imagem.</span><span class="sxs-lookup"><span data-stu-id="20a17-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="20a17-108">Abra o arquivo de imagem ISO e copie o arquivo boot. wim da pasta \\sources na imagem montada para um local no seu computador ou em uma unidade externa.</span><span class="sxs-lookup"><span data-stu-id="20a17-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="20a17-109">**Observação**  Se você gravou um CD ou DVD da imagem de recuperação, poderá abrir os arquivos no CD ou DVD e copiar o arquivo boot. wim da pasta \\sources.</span><span class="sxs-lookup"><span data-stu-id="20a17-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="20a17-110">Isso permite que você ignore a necessidade de montar a imagem.</span><span class="sxs-lookup"><span data-stu-id="20a17-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="20a17-111">Implante o arquivo boot. wim em um servidor WDS que possa ser acessado dos computadores de usuários finais na sua empresa.</span><span class="sxs-lookup"><span data-stu-id="20a17-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="20a17-112">Configure o servidor WDS para usar o arquivo boot. wim para DaRT seguindo seus procedimentos de implantação padrão do WDS.</span><span class="sxs-lookup"><span data-stu-id="20a17-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="20a17-113">Para obter mais informações sobre como implantar o DaRT como uma partição remota, consulte [passo a passo: implantar uma imagem usando o](https://go.microsoft.com/fwlink/?LinkId=212108) [Guia de introdução ao](https://go.microsoft.com/fwlink/?LinkId=212106)PXE e serviços de implantação do Windows.</span><span class="sxs-lookup"><span data-stu-id="20a17-113">For more information about how to deploy DaRT as a remote partition, see [Walkthrough: Deploy an Image by Using PXE](https://go.microsoft.com/fwlink/?LinkId=212108) and [Windows Deployment Services Getting Started Guide](https://go.microsoft.com/fwlink/?LinkId=212106).</span></span>

## <span data-ttu-id="20a17-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20a17-114">Related topics</span></span>


[<span data-ttu-id="20a17-115">Criação da imagem de recuperação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="20a17-115">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="20a17-116">Implantação da imagem de recuperação do DaRT</span><span class="sxs-lookup"><span data-stu-id="20a17-116">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="20a17-117">Planejamento para o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="20a17-117">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 





