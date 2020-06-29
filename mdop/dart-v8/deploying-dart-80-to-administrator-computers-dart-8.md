---
title: Implantar o DaRT 8.0 em computadores de administrador
description: Implantar o DaRT 8.0 em computadores de administrador
author: dansimp
ms.assetid: f918ead8-742e-464a-8bf6-1fcedde66cae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0ab001f612f2257ecbd77c39319cc99c17d36197
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799409"
---
# <span data-ttu-id="68254-103">Implantar o DaRT 8.0 em computadores de administrador</span><span class="sxs-lookup"><span data-stu-id="68254-103">Deploying DaRT 8.0 to Administrator Computers</span></span>


<span data-ttu-id="68254-104">Antes de começar a implantação do 8,0 (Microsoft Diagnostics and Recovery Toolset), examine os requisitos do seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="68254-104">Before you begin the deployment of Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, review the requirements for your environment.</span></span> <span data-ttu-id="68254-105">Isso inclui os requisitos de hardware para a instalação do DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="68254-105">This includes the hardware requirements for installing DaRT 8.0.</span></span> <span data-ttu-id="68254-106">Para obter mais informações sobre os requisitos de hardware e software do DaRT, consulte [configurações compatíveis com o dart 8,0](dart-80-supported-configurations-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="68254-106">For more information about DaRT hardware and software requirements, see [DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md).</span></span>

<span data-ttu-id="68254-107">Os tópicos desta seção podem ser usados para ajudar você a implantar o DaRT na sua empresa com base no ambiente e na estratégia de implantação.</span><span class="sxs-lookup"><span data-stu-id="68254-107">The topics in this section can be used to help you deploy DaRT in your enterprise based on your environment and deployment strategy.</span></span>

## <span data-ttu-id="68254-108">Implantar o DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="68254-108">Deploy DaRT 8.0</span></span>


<span data-ttu-id="68254-109">Você pode usar o arquivo do Windows Installer para o DaRT para instalar o DaRT em um computador que você usará primeiro para criar a imagem de recuperação do DaRT e, em seguida, solucionar e corrigir os computadores dos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="68254-109">You can use the Windows Installer file for DaRT to install DaRT on a computer that you will use to first create the DaRT recovery image and then troubleshoot and fix end-user computers.</span></span> <span data-ttu-id="68254-110">Frequentemente, em uma organização, você pode instalar no computador do administrador somente a funcionalidade do DaRT necessária para criar uma imagem de recuperação do DaRT.</span><span class="sxs-lookup"><span data-stu-id="68254-110">Frequently, across an organization, you might install on the administrator computer only the DaRT functionality that you need to create a DaRT recovery image.</span></span> <span data-ttu-id="68254-111">Em seguida, em um computador do administrador do suporte técnico, você pode instalar apenas a funcionalidade do DaRT que precisa ter para solucionar um problema com um computador, como o Visualizador de conexão remota do DaRT e o Crash Analyzer.</span><span class="sxs-lookup"><span data-stu-id="68254-111">Then, on a help desk administrator’s computer, you might install only the DaRT functionality that you must have to troubleshoot a problem computer, such as the DaRT Remote Connection Viewer and the Crash Analyzer.</span></span>

<span data-ttu-id="68254-112">Além de executar manualmente o arquivo do Windows Installer para instalar o DaRT, você também pode instalar o DaRT no prompt de comando para dar suporte a sistemas de implantação de software corporativo, como o SystemCenterConfigurationManager2012.</span><span class="sxs-lookup"><span data-stu-id="68254-112">In addition to manually running the Windows Installer file to install DaRT, you can also install DaRT at the command prompt to support enterprise software deployment systems such as SystemCenterConfigurationManager2012.</span></span>

[<span data-ttu-id="68254-113">Como implantar o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="68254-113">How to Deploy DaRT 8.0</span></span>](how-to-deploy-dart-80-dart-8.md)

## <span data-ttu-id="68254-114">Alterar, reparar ou remover o DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="68254-114">Change, repair, or remove DaRT 8.0</span></span>


<span data-ttu-id="68254-115">Você pode alterar, reparar ou remover a instalação do DaRT clicando duas vezes no arquivo de instalação do DaRT e, em seguida, clicando no botão que corresponde à ação que você deseja executar ou por meio do painel de controle do Windows.</span><span class="sxs-lookup"><span data-stu-id="68254-115">You can change, repair, or remove the DaRT installation by double-clicking the DaRT installation file and then clicking the button that corresponds to the action that you want to perform or through the Windows Control Panel.</span></span>

[<span data-ttu-id="68254-116">Como alterar, reparar ou remover o DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="68254-116">How to Change, Repair, or Remove DaRT 8.0</span></span>](how-to-change-repair-or-remove-dart-80-dart-8.md)

## <span data-ttu-id="68254-117">Como obter o DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="68254-117">How to get DaRT 8.0</span></span>


<span data-ttu-id="68254-118">Para obter o software DaRT, consulte [como obter o MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="68254-118">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="68254-119">Outros recursos para implantar o DaRT 8,0 em computadores administrador</span><span class="sxs-lookup"><span data-stu-id="68254-119">Other resources for deploying the DaRT 8.0 to administrator computers</span></span>


[<span data-ttu-id="68254-120">Implantação do DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="68254-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





