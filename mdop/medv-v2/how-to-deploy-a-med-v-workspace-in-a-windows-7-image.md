---
title: Como implantar um espaço de trabalho da MED-V em uma imagem do Windows 7
description: Como implantar um espaço de trabalho da MED-V em uma imagem do Windows 7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10800041"
---
# <span data-ttu-id="1cb8e-103">Como implantar um espaço de trabalho da MED-V em uma imagem do Windows 7</span><span class="sxs-lookup"><span data-stu-id="1cb8e-103">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>


<span data-ttu-id="1cb8e-104">Você pode instalar todos os componentes do MED-V em uma imagem do Windows 7 que você distribui em toda a sua empresa da mesma forma que faria com qualquer nova instalação do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-104">You can install all the MED-V components into a Windows 7 image that you distribute throughout your enterprise just as you would any new installation of Windows 7.</span></span> <span data-ttu-id="1cb8e-105">Em seguida, o usuário final conclui a instalação do espaço de trabalho do MED-V clicando em um atalho do menu **Iniciar** que você configura para iniciar o MED-v.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-105">The end user then finishes the installation of the MED-V workspace by clicking a **Start** menu shortcut that you configure to start MED-V.</span></span> <span data-ttu-id="1cb8e-106">Primeira vez que a configuração iniciar e o usuário final seguir as instruções para concluir a configuração.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-106">First time setup starts and the end user follows the instructions to complete the configuration.</span></span>

<span data-ttu-id="1cb8e-107">A seção a seguir fornece informações e instruções para ajudá-lo a implantar o espaço de trabalho do MED-V em toda a sua empresa usando uma imagem do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-107">The following section provides information and instructions to help you deploy the MED-V workspace throughout your enterprise by using a Windows 7 image.</span></span>

**<span data-ttu-id="1cb8e-108">Para implantar um espaço de trabalho do MED-V em uma imagem do Windows 7</span><span class="sxs-lookup"><span data-stu-id="1cb8e-108">To deploy a MED-V workspace in a Windows 7 image</span></span>**

1.  <span data-ttu-id="1cb8e-109">Crie uma imagem padrão do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-109">Create a standard image of Windows 7.</span></span> <span data-ttu-id="1cb8e-110">Para obter mais informações, consulte [criando uma imagem padrão do Windows 7: guia](https://go.microsoft.com/fwlink/?LinkId=204843) passo a passo ( https://go.microsoft.com/fwlink/?LinkId=204843) .</span><span class="sxs-lookup"><span data-stu-id="1cb8e-110">For more information, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=204843) (https://go.microsoft.com/fwlink/?LinkId=204843).</span></span>

2.  <span data-ttu-id="1cb8e-111">Na imagem do Windows 7, instale o PC virtual do Windows e as atualizações do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-111">In the Windows 7 image, install Windows Virtual PC and the Windows Virtual PC updates.</span></span> <span data-ttu-id="1cb8e-112">Para obter mais informações, consulte [configurar pré-requisitos de instalação](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="1cb8e-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

3.  <span data-ttu-id="1cb8e-113">Instale o agente de host do MED-V usando o arquivo de instalação do MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-113">Install the MED-V Host Agent by using the MED-V\_HostAgent\_Setup installation file.</span></span> <span data-ttu-id="1cb8e-114">Para obter mais informações, consulte [como instalar manualmente o agente de host do MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="1cb8e-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    <span data-ttu-id="1cb8e-115">**Aviso**  O Internet Explorer deve ser fechado antes de instalar o agente de host do MED-V, caso contrário, pode ocorrer conflitos mais tarde com o redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-115">**Warning** Internet Explorer must be closed before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="1cb8e-116">Você também pode fazer isso especificando uma reinicialização do computador durante uma distribuição.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-116">You can also do this by specifying a computer restart during a distribution.</span></span>

     

4.  <span data-ttu-id="1cb8e-117">Copie os arquivos de pacote do espaço de trabalho do MED-V para a imagem do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-117">Copy the MED-V workspace package files to the Windows 7 image.</span></span> <span data-ttu-id="1cb8e-118">Os arquivos de pacote do espaço de trabalho do MED-V são o arquivo de espaço de trabalho do MED-V, o arquivo. medv e o arquivo de setup.exe que você criou usando o **pacote do espaço de trabalho do MED-v**.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-118">The MED-V workspace package files are the MED-V workspace installer, .medv file, and setup.exe file that you created by using the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="1cb8e-119">**Importante**  O arquivo. medv e setup.exe deve estar na mesma pasta que o instalador do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-119">**Important** The .medv and setup.exe file must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="1cb8e-120">Em seguida, instale o espaço de trabalho do MED-V executando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-120">Then, install the MED-V workspace by running setup.exe.</span></span>

     

5.  <span data-ttu-id="1cb8e-121">Configurar um atalho no menu **Iniciar** para abrir a instalação do pacote do espaço de trabalho do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-121">Configure a shortcut on the **Start** menu to open the MED-V workspace package installation.</span></span>

    <span data-ttu-id="1cb8e-122">Crie um atalho do menu **Iniciar** para o arquivo setup.exe que permite ao usuário final iniciar uma instalação do MED-V conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-122">Create a **Start** menu shortcut to the setup.exe file that lets the end user start a MED-V installation as required.</span></span>

6.  <span data-ttu-id="1cb8e-123">Usando o processo de implantação de imagens padrão da sua empresa, distribua a imagem do Windows 7 para os computadores da sua empresa que exigem o MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-123">By using your company’s standard image deployment process, distribute the Windows 7 image to computers in your enterprise that require MED-V.</span></span>

<span data-ttu-id="1cb8e-124">Quando o usuário final precisa acessar um aplicativo publicado no espaço de trabalho do MED-V, ele pode clicar no atalho do menu **Iniciar** para instalar o espaço de trabalho do MED-v.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-124">When the end user has to access an application published in the MED-V workspace, they can click the **Start** menu shortcut to install the MED-V workspace.</span></span> <span data-ttu-id="1cb8e-125">Isso iniciará automaticamente a instalação da primeira vez e concluirá a configuração do MED-V.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-125">This automatically starts first time setup and completes the configuration of MED-V.</span></span> <span data-ttu-id="1cb8e-126">Depois que a configuração for concluída pela primeira vez, o usuário final poderá acessar os aplicativos MED-V no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="1cb8e-126">After first time setup is complete, the end user can access the MED-V applications on the **Start** menu.</span></span>

## <span data-ttu-id="1cb8e-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1cb8e-127">Related topics</span></span>


[<span data-ttu-id="1cb8e-128">Visão geral da implantação da MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="1cb8e-128">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="1cb8e-129">Como implantar um espaço de trabalho da MED-V por meio de um sistema de distribuição eletrônica de software</span><span class="sxs-lookup"><span data-stu-id="1cb8e-129">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





