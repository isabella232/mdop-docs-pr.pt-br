---
title: Instalar aplicativos em uma imagem do Windows Virtual PC
description: Instalar aplicativos em uma imagem do Windows Virtual PC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799951"
---
# <span data-ttu-id="5ce0a-103">Instalar aplicativos em uma imagem do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5ce0a-103">Installing Applications on a Windows Virtual PC Image</span></span>


<span data-ttu-id="5ce0a-104">Depois de criar uma imagem do PC virtual do Windows para uso com o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, você pode instalar outros componentes que sejam úteis ao executar o MED-V, como um sistema ESD (distribuição de software eletrônico) e um software antivírus.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-104">After you have created a Windows Virtual PC image for use with Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you can install other components that are helpful when running MED-V, such as an electronic software distribution (ESD) system and antivirus software.</span></span>

<span data-ttu-id="5ce0a-105">A seção a seguir fornece informações para ajudá-lo a instalar o software na imagem do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-105">The following section provides information to help you install software on the MED-V image.</span></span>

<span data-ttu-id="5ce0a-106">**Cuidado**  Para facilitar o gerenciamento do espaço de trabalho do MED-V após a implantação, recomendamos que você limite o número de componentes que você instala na imagem do MED-V para os componentes necessários ou que sejam úteis ao usar o MED-V.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-106">**Caution** For ease of MED-V workspace management after deployment, we recommend that you limit the number of components that you install on the MED-V image to those components that are required or that are helpful when using MED-V.</span></span> <span data-ttu-id="5ce0a-107">Por exemplo, embora não seja necessário executar o MED-V, você pode instalar um sistema ESD para usar mais tarde para instalar aplicativos em um espaço de trabalho do MED-V e software antivírus para segurança na imagem.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-107">For example, although they are not required to run MED-V, you can install an ESD system to use later for installing applications to a MED-V workspace and antivirus software for security on the image.</span></span>

 

**<span data-ttu-id="5ce0a-108">Instalando o software em uma imagem do MED-V</span><span class="sxs-lookup"><span data-stu-id="5ce0a-108">Installing Software on a MED-V Image</span></span>**

1.  <span data-ttu-id="5ce0a-109">Se não estiver sendo executado no momento, abra sua máquina virtual do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-109">If it is not currently running, open your MED-V virtual machine.</span></span>

    1.  <span data-ttu-id="5ce0a-110">Clique em **Iniciar**, clique em **todos os programas**, clique em **PC virtual do Windows** e clique em **PC virtual do Windows**.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-110">Click **Start**, click **All Programs**, click **Windows Virtual PC** and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="5ce0a-111">Clique duas vezes em sua máquina virtual do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-111">Double-click your MED-V virtual machine.</span></span>

2.  <span data-ttu-id="5ce0a-112">De dentro do sistema operacional da máquina virtual, localize os arquivos de instalação do software que você deseja instalar.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-112">From inside the virtual machine operating system, locate the installation files for the software that you want to install.</span></span>

3.  <span data-ttu-id="5ce0a-113">Siga as instruções de instalação fornecidas pelo fornecedor do software.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-113">Follow the installation instructions that are provided by the software vendor.</span></span>

    <span data-ttu-id="5ce0a-114">**Observação**  Após a conclusão da instalação, talvez seja necessário fechar e reiniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-114">**Note** After installation is complete, you might have to close and then restart the virtual machine.</span></span>

     

<span data-ttu-id="5ce0a-115">Repita essas etapas para qualquer software ou aplicativo que você queira instalar na imagem do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-115">Repeat these steps for any software or application that you want to install on the MED-V image.</span></span> <span data-ttu-id="5ce0a-116">Recomendamos que você limite o número de aplicativos que você pré-instalando na imagem.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-116">We recommend that you limit the number of applications that you preinstall on the image.</span></span> <span data-ttu-id="5ce0a-117">O processo recomendado para instalar aplicativos e outros softwares na imagem é pré-instalar um sistema ESD agora e usá-lo posteriormente para implantar o software na imagem.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-117">The recommended process for installing applications and other software on the image is to preinstall an ESD system now and to use it later to deploy software to the image.</span></span> <span data-ttu-id="5ce0a-118">Como alternativa, você também pode usar a política de grupo ou o App-V para adicionar ou remover aplicativos em um espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-118">Alternately, you can also use Group Policy or App-V to add or remove applications on a MED-V workspace.</span></span> <span data-ttu-id="5ce0a-119">Para obter mais informações, consulte [Gerenciando aplicativos implantados em espaços de trabalho do MED-V](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="5ce0a-119">For more information, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

<span data-ttu-id="5ce0a-120">Para obter mais informações sobre como instalar software em uma imagem virtual, consulte os seguintes artigos:</span><span class="sxs-lookup"><span data-stu-id="5ce0a-120">For more information about how to install software on a virtual image, see the following articles:</span></span>

-   <span data-ttu-id="5ce0a-121">[Publicar e usar aplicativos virtuais](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .</span><span class="sxs-lookup"><span data-stu-id="5ce0a-121">[Publish and Use Virtual Applications](https://go.microsoft.com/fwlink/?LinkId=195926) (https://go.microsoft.com/fwlink/?LinkId=195926).</span></span>

-   <span data-ttu-id="5ce0a-122">[Ajuda do Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="5ce0a-122">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="5ce0a-123">Depois de instalar todo o software que você deseja na imagem do MED-V, sua imagem estará pronta para ser empacotada.</span><span class="sxs-lookup"><span data-stu-id="5ce0a-123">After you have installed all of the software that you want on the MED-V image, your image is ready to be packaged.</span></span>

## <span data-ttu-id="5ce0a-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ce0a-124">Related topics</span></span>


[<span data-ttu-id="5ce0a-125">Como configurar uma imagem do Windows Virtual PC para a MED-V</span><span class="sxs-lookup"><span data-stu-id="5ce0a-125">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="5ce0a-126">Preparar uma imagem da MED-V</span><span class="sxs-lookup"><span data-stu-id="5ce0a-126">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)

 

 





