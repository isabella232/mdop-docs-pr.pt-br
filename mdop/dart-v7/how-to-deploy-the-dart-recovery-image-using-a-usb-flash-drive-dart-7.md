---
title: Como implantar a imagem de recuperação do DaRT usando um pen drive
description: Como implantar a imagem de recuperação do DaRT usando um pen drive
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799318"
---
# <span data-ttu-id="7600f-103">Como implantar a imagem de recuperação do DaRT usando um pen drive</span><span class="sxs-lookup"><span data-stu-id="7600f-103">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="7600f-104">Após concluir a execução do **Assistente de imagem de recuperação DART**, você pode usar a ferramenta em <https://go.microsoft.com/fwlink/?LinkId=218888> para copiar o arquivo de imagem ISO para uma unidade flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="7600f-104">After you have finished running the **DaRT Recovery Image Wizard**, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

<span data-ttu-id="7600f-105">Você também pode copiar manualmente o arquivo de imagem ISO para um UFD seguindo as etapas fornecidas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="7600f-105">You can also manually copy the ISO image file to a UFD by following the steps provided in this section.</span></span>

**<span data-ttu-id="7600f-106">Para salvar a imagem de recuperação do DaRT em uma unidade flash USB</span><span class="sxs-lookup"><span data-stu-id="7600f-106">To save the DaRT recovery image to a USB flash drive</span></span>**

1.  <span data-ttu-id="7600f-107">Formate a unidade flash USB.</span><span class="sxs-lookup"><span data-stu-id="7600f-107">Format the USB flash drive.</span></span>

    1.  <span data-ttu-id="7600f-108">Em um sistema operacional válido ou uma sessão do WindowsPE válida, insira seu UFD.</span><span class="sxs-lookup"><span data-stu-id="7600f-108">From a running valid operating system or WindowsPE session, insert your UFD.</span></span>

    2.  <span data-ttu-id="7600f-109">No prompt de comando com permissões de administrador, digite **DiskPart** e digite **list disk**.</span><span class="sxs-lookup"><span data-stu-id="7600f-109">At the command prompt with administrator permissions, type **DISKPART** and then type **LIST DISK**.</span></span>

        <span data-ttu-id="7600f-110">A janela do prompt de comando exibe o número do disco do UFD, por exemplo, o **disco 1**.</span><span class="sxs-lookup"><span data-stu-id="7600f-110">The Command Prompt window displays the disk number of your UFD, for example **DISK 1**.</span></span>

    3.  <span data-ttu-id="7600f-111">Insira os comandos a seguir, um por vez, no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="7600f-111">Enter the following commands one at a time at the command prompt.</span></span>

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        <span data-ttu-id="7600f-112">**Observação**  O exemplo de código anterior pressupõe DISK1 é o UFD.</span><span class="sxs-lookup"><span data-stu-id="7600f-112">**Note** The previous code example assumes Disk1 is the UFD.</span></span> <span data-ttu-id="7600f-113">Se for necessário, substitua o disco 1 pelo número do seu disco.</span><span class="sxs-lookup"><span data-stu-id="7600f-113">If it is necessary, replace DISK 1 with your disk number.</span></span>

         

2.  <span data-ttu-id="7600f-114">Usando o método preferido da sua empresa para montar uma imagem, monte o arquivo de imagem ISO que você criou na caixa de diálogo **criar imagem de inicialização** do **Assistente de imagem de recuperação do DART**.</span><span class="sxs-lookup"><span data-stu-id="7600f-114">By using your company’s preferred method of mounting an image, mount the ISO image file that you created in the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="7600f-115">Isso requer que você tenha um método disponível para montar um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="7600f-115">This requires that you have a method available to mount an image file.</span></span>

3.  <span data-ttu-id="7600f-116">Abra o arquivo de imagem ISO montado e copie todo o seu conteúdo para a unidade flash USB formatada.</span><span class="sxs-lookup"><span data-stu-id="7600f-116">Open the mounted ISO image file and copy all its contents to the formatted USB flash drive.</span></span>

    <span data-ttu-id="7600f-117">**Observação**  Se você gravou um CD ou DVD da imagem de recuperação, poderá abrir os arquivos no CD ou DVD e copiar o conteúdo para o UFD.</span><span class="sxs-lookup"><span data-stu-id="7600f-117">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the contents to the UFD.</span></span> <span data-ttu-id="7600f-118">Isso permite que você ignore a necessidade de montar a imagem.</span><span class="sxs-lookup"><span data-stu-id="7600f-118">This lets you skip the need to mount the image.</span></span>

     

## <span data-ttu-id="7600f-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7600f-119">Related topics</span></span>


[<span data-ttu-id="7600f-120">Implantação da imagem de recuperação do DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7600f-120">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





