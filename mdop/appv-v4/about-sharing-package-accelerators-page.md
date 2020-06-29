---
title: Página Sobre Aceleradores de Pacote
description: Página Sobre Aceleradores de Pacote
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797636"
---
# <span data-ttu-id="78235-103">Página Sobre Aceleradores de Pacote</span><span class="sxs-lookup"><span data-stu-id="78235-103">About Sharing Package Accelerators Page</span></span>


<span data-ttu-id="78235-104">As informações a seguir fornecem informações de práticas recomendadas sobre como compartilhar aceleradores de pacote.</span><span class="sxs-lookup"><span data-stu-id="78235-104">This following information provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="78235-105">Se você planeja compartilhar arquivos de aceleradores de pacote, informações como nomes de computador, informações da conta do usuário e informações sobre aplicativos incluídos nas transformações podem estar incluídas no arquivo aceleradores de pacote.</span><span class="sxs-lookup"><span data-stu-id="78235-105">If you plan to share Package Accelerators files, information such as computer names, user account information, and information about applications included in the transforms might be included in the Package Accelerators file.</span></span> <span data-ttu-id="78235-106">Você deve examinar quaisquer configurações ou arquivos de configuração associados ao pacote de aplicativo virtual para garantir que os aplicativos não contenham informações pessoais. Esta página contém os elementos a seguir.</span><span class="sxs-lookup"><span data-stu-id="78235-106">You should review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.This page contains the following elements.</span></span>

-   <span data-ttu-id="78235-107">**Nome de usuário**.</span><span class="sxs-lookup"><span data-stu-id="78235-107">**Username**.</span></span> <span data-ttu-id="78235-108">Ao fazer logon no computador executando o Microsoft App-V Sequencer, você deve usar uma conta de usuário genérica, como a conta de **administrador** interna.</span><span class="sxs-lookup"><span data-stu-id="78235-108">When you log on to the computer running the Microsoft App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account.</span></span> <span data-ttu-id="78235-109">Você não deve usar uma conta com base em um nome de usuário existente.</span><span class="sxs-lookup"><span data-stu-id="78235-109">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="78235-110">**Nome do computador**.</span><span class="sxs-lookup"><span data-stu-id="78235-110">**Computer Name**.</span></span> <span data-ttu-id="78235-111">Especifique um nome geral, não identificado do computador que está executando o sequenciador.</span><span class="sxs-lookup"><span data-stu-id="78235-111">Specify a general, non-identifying name of the computer running the Sequencer.</span></span>

-   <span data-ttu-id="78235-112">**URL do servidor**.</span><span class="sxs-lookup"><span data-stu-id="78235-112">**Server URL**.</span></span> <span data-ttu-id="78235-113">No console App-V Sequencer, na guia **implantação** , use as configurações padrão para as informações de configuração de URL do servidor.</span><span class="sxs-lookup"><span data-stu-id="78235-113">In the App-V Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="78235-114">**Aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="78235-114">**Applications**.</span></span> <span data-ttu-id="78235-115">Se você não deseja compartilhar a lista de aplicativos que foram instalados no computador que executa o sequenciador quando você criou o acelerador de pacote, você deve excluir o arquivo **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="78235-115">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="78235-116">Esse arquivo está localizado no diretório raiz do pacote do pacote de aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="78235-116">This file is located in the package root directory of the virtual application package.</span></span>

## <span data-ttu-id="78235-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78235-117">Related topics</span></span>


[<span data-ttu-id="78235-118">Assistente para Criar Acelerador de Pacote (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="78235-118">Create Package Accelerator Wizard (AppV 4.6 SP1)</span></span>](create-package-accelerator-wizard--appv-46-sp1-.md)

[<span data-ttu-id="78235-119">Sobre aceleradores de pacote do App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="78235-119">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





