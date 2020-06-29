---
title: Como alterar as propriedades da implantação
description: Como alterar as propriedades da implantação
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797250"
---
# <span data-ttu-id="3a2bb-103">Como alterar as propriedades da implantação</span><span class="sxs-lookup"><span data-stu-id="3a2bb-103">How to Change Deployment Properties</span></span>


<span data-ttu-id="3a2bb-104">Você pode usar os procedimentos a seguir para alterar as informações da guia de **implantação** para um aplicativo que você está sequenciando, incluindo a URL do servidor de virtualização de aplicativos, os sistemas operacionais necessários para os aplicativos virtualizados e as opções de saída para o aplicativo virtual a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-104">You can use the following procedures to change the **Deployment** tab information for an application you are sequencing, including the Application Virtualization server URL, the operating systems required by the virtualized applications, and the output options for the virtual application to be installed.</span></span>

**<span data-ttu-id="3a2bb-105">Para alterar a URL do servidor</span><span class="sxs-lookup"><span data-stu-id="3a2bb-105">To change the server URL</span></span>**

1.  <span data-ttu-id="3a2bb-106">Selecione o protocolo de streaming na caixa de listagem suspensa.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-106">Select the streaming protocol from the drop-down list box.</span></span>

2.  <span data-ttu-id="3a2bb-107">Digite o nome do host do servidor de aplicativos virtual ou o balanceador de carga do grupo do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-107">Enter the host name of the virtual application server or the server group's load balancer.</span></span> <span data-ttu-id="3a2bb-108">Você pode usar o nome do host ou endereço IP real.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-108">You can use the actual host name or IP address.</span></span>

3.  <span data-ttu-id="3a2bb-109">Especifique o número da porta na qual o servidor de aplicativos virtual ou o balanceador de carga escutará uma solicitação de cliente da área de trabalho do aplicativo Virtualization para o aplicativo em fluxo.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-109">Specify the port number on which the virtual application server or load balancer will listen for an Application Virtualization Desktop Client request for the streamed application.</span></span>

4.  <span data-ttu-id="3a2bb-110">Especifique o caminho relativo no servidor de aplicativos virtual em que o pacote do software está armazenado.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-110">Specify the relative path on the virtual application server where the software package is stored.</span></span>

**<span data-ttu-id="3a2bb-111">Para alterar os requisitos do sistema operacional do aplicativo</span><span class="sxs-lookup"><span data-stu-id="3a2bb-111">To change the application operating systems requirements</span></span>**

1.  <span data-ttu-id="3a2bb-112">Para adicionar o (s) sistema (es) operacional necessário (s), selecione-o na lista **disponível** e clique no botão de seta apontando para o controle de lista de sistemas operacionais **selecionados** .</span><span class="sxs-lookup"><span data-stu-id="3a2bb-112">To add the required operating system(s), select it in the **Available** list and click the arrow button pointing to the **Selected** operating systems list control.</span></span>

2.  <span data-ttu-id="3a2bb-113">Para remover um sistema operacional, selecione-o no controle de lista **selecionado** e clique no botão de seta apontando para o controle de lista de sistemas operacionais **disponíveis** .</span><span class="sxs-lookup"><span data-stu-id="3a2bb-113">To remove an operating system, select it in the **Selected** list control, and click the arrow button pointing to the **Available** operating systems list control.</span></span>

**<span data-ttu-id="3a2bb-114">Para alterar as opções de saída do aplicativo</span><span class="sxs-lookup"><span data-stu-id="3a2bb-114">To change the application output options</span></span>**

1.  <span data-ttu-id="3a2bb-115">Na lista suspensa **algoritmo de compactação** , selecione o método de compactação a ser usado ao transmitir o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-115">From the **Compression Algorithm** drop-down list, select the compression method to use when streaming the application.</span></span>

2.  <span data-ttu-id="3a2bb-116">Marque a caixa de seleção **impor descritores de segurança** para garantir que os descritores de segurança dos aplicativos em pacotes sejam aplicados quando implantados.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-116">Select the **Enforce Security Descriptors** check box to ensure security descriptors of the packaged applications are enforced when deployed.</span></span>

3.  <span data-ttu-id="3a2bb-117">Selecione **gerar arquivo de diferença** para gerar um arquivo de diferença para o aplicativo da versão sequenciada anterior.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-117">Select **Generate Difference File** to generate a difference file for the application from the previous sequenced version.</span></span>

4.  <span data-ttu-id="3a2bb-118">Selecione **gerar pacote do Microsoft Windows Installer (MSI)** para criar um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="3a2bb-118">Select **Generate Microsoft Windows Installer (MSI) Package** to create an installer package.</span></span>

## <span data-ttu-id="3a2bb-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3a2bb-119">Related topics</span></span>


[<span data-ttu-id="3a2bb-120">Sobre a guia Implantação</span><span class="sxs-lookup"><span data-stu-id="3a2bb-120">About the Deployment Tab</span></span>](about-the-deployment-tab.md)

[<span data-ttu-id="3a2bb-121">Console do Sequencer</span><span class="sxs-lookup"><span data-stu-id="3a2bb-121">Sequencer Console</span></span>](sequencer-console.md)

 

 





