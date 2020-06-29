---
title: Como instalar o sequenciador
description: Como instalar o sequenciador
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797091"
---
# <span data-ttu-id="a4bae-103">Como instalar o sequenciador</span><span class="sxs-lookup"><span data-stu-id="a4bae-103">How to Install the Sequencer</span></span>


<span data-ttu-id="a4bae-104">O sequenciador do Microsoft Application Virtualization (App-V) monitora e registra o processo de instalação e configuração de aplicativos para que o aplicativo possa ser executado como um aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="a4bae-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records the installation and setup process for applications so that the application can be run as a virtual application.</span></span> <span data-ttu-id="a4bae-105">Você deve instalar o sequenciador em um computador que tenha somente o sistema operacional instalado.</span><span class="sxs-lookup"><span data-stu-id="a4bae-105">You should install the Sequencer on a computer that has only the operating system installed.</span></span> <span data-ttu-id="a4bae-106">Você também pode instalar o sequenciador em um computador que executa um ambiente virtual, por exemplo, Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a4bae-106">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="a4bae-107">Esse método é útil porque é mais fácil manter um ambiente de sequenciamento de limpeza que pode ser reutilizado com configuração adicional mínima.</span><span class="sxs-lookup"><span data-stu-id="a4bae-107">This method is useful because it is easier to maintain a clean sequencing environment that can be reused with minimal additional configuration.</span></span>

<span data-ttu-id="a4bae-108">Você deve ter direitos administrativos no computador que você está usando para sequenciar o aplicativo e o computador deve estar conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="a4bae-108">You must have administrative rights on the computer you are using to sequence the application and the computer must be connected to the network.</span></span> <span data-ttu-id="a4bae-109">O computador não deve estar executando nenhuma versão do cliente do Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="a4bae-109">The computer must not be running any version of the Application Virtualization (App-V) client.</span></span> <span data-ttu-id="a4bae-110">A criação de um aplicativo virtual usando o sequenciador exige muitos recursos, portanto, é importante que você instale o sequenciador em um computador que atenda ou exceda os requisitos recomendados.</span><span class="sxs-lookup"><span data-stu-id="a4bae-110">Creating a virtual application using the Sequencer is very resource intensive, so it is important that you install the Sequencer on a computer that meets or exceeds the recommended requirements.</span></span> <span data-ttu-id="a4bae-111">Para obter mais informações sobre os requisitos do sistema, consulte [requisitos de hardware e software do sequenciador](sequencer-hardware-and-software-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4bae-111">For more information about the system requirements, see [Sequencer Hardware and Software Requirements](sequencer-hardware-and-software-requirements.md)..</span></span>

**<span data-ttu-id="a4bae-112">Para instalar o Microsoft Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="a4bae-112">To install the Microsoft Application Virtualization Sequencer</span></span>**

1.  <span data-ttu-id="a4bae-113">Copie os arquivos de instalação do Microsoft Application Virtualization Sequencer para o computador em que você deseja instalá-lo.</span><span class="sxs-lookup"><span data-stu-id="a4bae-113">Copy the Microsoft Application Virtualization Sequencer installation files to the computer that you want to install it on.</span></span>

2.  <span data-ttu-id="a4bae-114">Para iniciar o assistente de instalação do Microsoft Application Virtualization Sequencer, selecione **setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="a4bae-114">To start the Microsoft Application Virtualization Sequencer installation wizard, select **setup.exe**.</span></span> <span data-ttu-id="a4bae-115">Se o **Microsoft Visual C++ SP1 Redistributable Package (x86)** não for detectado antes da instalação, o **setup.exe** será instalado.</span><span class="sxs-lookup"><span data-stu-id="a4bae-115">If the **Microsoft Visual C++ SP1 Redistributable Package (x86)** is not detected prior to installation, **setup.exe** will install it.</span></span>

3.  <span data-ttu-id="a4bae-116">Na página de **boas-vindas** , clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a4bae-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="a4bae-117">Na página **contrato de licença** , para aceitar os termos do contrato de licença, selecione **aceito os termos do contrato de licença**.</span><span class="sxs-lookup"><span data-stu-id="a4bae-117">On the **License Agreement** page, to accept the terms of the license agreement, select **I accept the terms in the license agreement**.</span></span> <span data-ttu-id="a4bae-118">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a4bae-118">Click **Next**.</span></span>

5.  <span data-ttu-id="a4bae-119">Na página **pasta de destino** , para aceitar a pasta de instalação padrão, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a4bae-119">On the **Destination Folder** page, to accept the default installation folder, click **Next**.</span></span> <span data-ttu-id="a4bae-120">Para especificar uma pasta de destino diferente, clique em **alterar** e especifique a pasta de instalação que será usada para a instalação.</span><span class="sxs-lookup"><span data-stu-id="a4bae-120">To specify a different destination folder, click **Change** and specify the installation folder that will be used for the installation.</span></span> <span data-ttu-id="a4bae-121">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="a4bae-121">Click **Next**.</span></span>

6.  <span data-ttu-id="a4bae-122">Na página **pronto para instalar o programa** , clique em **instalar**para iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="a4bae-122">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="a4bae-123">Na página **Assistente InstallShield concluído** , para fechar o assistente de instalação e abrir o sequenciador, clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="a4bae-123">On the **InstallShield Wizard Completed** page, to close the installation wizard and open the Sequencer, click **Finish**.</span></span> <span data-ttu-id="a4bae-124">Para fechar o assistente de instalação sem abrir o sequenciador, desmarque **iniciar o programa** e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="a4bae-124">To close the installation wizard without opening the Sequencer, deselect **Launch the program** and click **Finish**.</span></span>

## <span data-ttu-id="a4bae-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4bae-125">Related topics</span></span>


[<span data-ttu-id="a4bae-126">Configurando o Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="a4bae-126">Configuring the Application Virtualization Sequencer</span></span>](configuring-the-application-virtualization-sequencer.md)

 

 





