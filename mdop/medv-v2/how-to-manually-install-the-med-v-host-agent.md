---
title: Como instalar manualmente o agente de host da MED-V
description: Como instalar manualmente o agente de host da MED-V
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796114"
---
# <span data-ttu-id="510d6-103">Como instalar manualmente o agente de host da MED-V</span><span class="sxs-lookup"><span data-stu-id="510d6-103">How to Manually Install the MED-V Host Agent</span></span>


<span data-ttu-id="510d6-104">Há dois componentes separados, mas relacionados à solução de virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0: o agente de host e o agente de convidado do MED-V.</span><span class="sxs-lookup"><span data-stu-id="510d6-104">There are two separate but related components to the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="510d6-105">O agente do host reside no computador host (um computador do usuário que está executando o Windows 7) e fornece um canal para se comunicar com o convidado do MED-V (a máquina virtual do MED-V em execução no computador host).</span><span class="sxs-lookup"><span data-stu-id="510d6-105">The Host Agent resides on the host computer (a user’s computer that is running Windows 7) and provides a channel to communicate with the MED-V guest (the MED-V virtual machine running in the host computer).</span></span> <span data-ttu-id="510d6-106">Ele também fornece certas funcionalidades relacionadas ao MED-V, como a publicação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="510d6-106">It also provides certain MED-V related functionality, such as application publishing.</span></span>

<span data-ttu-id="510d6-107">Geralmente, você implanta e instala o agente de host do MED-V usando o método preferencial de provisionamento da sua empresa.</span><span class="sxs-lookup"><span data-stu-id="510d6-107">Typically, you deploy and install the MED-V Host Agent by using your company’s preferred method of provisioning software.</span></span> <span data-ttu-id="510d6-108">No entanto, antes de implantar o MED-V em toda a sua empresa, talvez você prefira instalar o agente do host localmente para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="510d6-108">However, before deploying MED-V across your enterprise, you might prefer to install the Host Agent locally for testing.</span></span> <span data-ttu-id="510d6-109">Esta seção fornece instruções passo a passo para instalar manualmente o agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="510d6-109">This section provides step-by-step instructions for manually installing the MED-V Host Agent.</span></span>

<span data-ttu-id="510d6-110">**Observação**  O agente de convidado do MED-V é instalado automaticamente durante a primeira configuração.</span><span class="sxs-lookup"><span data-stu-id="510d6-110">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<span data-ttu-id="510d6-111">**Importante**  Feche o Internet Explorer antes de instalar o agente de host do MED-V, caso contrário, pode ocorrer conflitos mais tarde com o redirecionamento de URL.</span><span class="sxs-lookup"><span data-stu-id="510d6-111">**Important** Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="510d6-112">Você também pode fazer isso especificando uma reinicialização do computador durante uma distribuição.</span><span class="sxs-lookup"><span data-stu-id="510d6-112">You can also do this by specifying a computer restart during a distribution.</span></span>

 

**<span data-ttu-id="510d6-113">Para instalar o agente de host do MED-V</span><span class="sxs-lookup"><span data-stu-id="510d6-113">To install the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="510d6-114">Localize os arquivos de instalação do MED-V recebidos como parte do download do software.</span><span class="sxs-lookup"><span data-stu-id="510d6-114">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="510d6-115">Clique duas vezes no arquivo de instalação do MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="510d6-115">Double-click the MED-V\_HostAgent\_Setup installation file.</span></span>

    <span data-ttu-id="510d6-116">O assistente de **configuração do agente de host do Microsoft Enterprise Desktop Virtualization (MED-V)** é aberto.</span><span class="sxs-lookup"><span data-stu-id="510d6-116">The **Microsoft Enterprise Desktop Virtualization (MED-V) Host Agent Setup** wizard opens.</span></span> <span data-ttu-id="510d6-117">Clique em **Avançar** para continuar.</span><span class="sxs-lookup"><span data-stu-id="510d6-117">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="510d6-118">Aceite os termos de licença para software Microsoft e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="510d6-118">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="510d6-119">Selecione a pasta de destino para instalar o agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="510d6-119">Select the destination folder for installing the MED-V Host Agent.</span></span> <span data-ttu-id="510d6-120">Clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="510d6-120">Click **Next**.</span></span>

5.  <span data-ttu-id="510d6-121">Para começar a instalação do Host Agent, clique em **instalar**.</span><span class="sxs-lookup"><span data-stu-id="510d6-121">To begin the Host Agent installation, click **Install**.</span></span>

6.  <span data-ttu-id="510d6-122">Depois que a instalação for concluída com êxito, clique em **concluir** para fechar o assistente.</span><span class="sxs-lookup"><span data-stu-id="510d6-122">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="510d6-123">Para verificar se a instalação do agente do host foi bem-sucedida, clique em **Iniciar**, em **todos os programas**, em **virtualização de área de trabalho do Microsoft Enterprise**e clique em **agente de host do MED-V**.</span><span class="sxs-lookup"><span data-stu-id="510d6-123">To verify that the installation of the Host Agent was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="510d6-124">**Observação**  Até que um espaço de trabalho do MED-V seja instalado, o agente de host do MED-V pode ser iniciado e executado, mas não oferece funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="510d6-124">**Note** Until a MED-V workspace is installed, the MED-V Host Agent can be started and runs, but provides no functionality.</span></span>

 

## <span data-ttu-id="510d6-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="510d6-125">Related topics</span></span>


[<span data-ttu-id="510d6-126">Como implantar os componentes da MED-V por meio de um sistema de distribuição eletrônica de software</span><span class="sxs-lookup"><span data-stu-id="510d6-126">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="510d6-127">Como instalar o empacotador de espaço de trabalho da MED-V</span><span class="sxs-lookup"><span data-stu-id="510d6-127">How to Install the MED-V Workspace Packager</span></span>](how-to-install-the-med-v-workspace-packager.md)

[<span data-ttu-id="510d6-128">Como desinstalar os componentes da MED-V</span><span class="sxs-lookup"><span data-stu-id="510d6-128">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





