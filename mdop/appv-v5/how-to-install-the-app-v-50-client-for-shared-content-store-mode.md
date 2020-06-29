---
title: Como instalar o cliente App-V 5.0 para o modo de repositório de conteúdo compartilhado
description: Como instalar o cliente App-V 5.0 para o modo de repositório de conteúdo compartilhado
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796404"
---
# <span data-ttu-id="3e047-103">Como instalar o cliente App-V 5.0 para o modo de repositório de conteúdo compartilhado</span><span class="sxs-lookup"><span data-stu-id="3e047-103">How to Install the App-V 5.0 Client for Shared Content Store Mode</span></span>


<span data-ttu-id="3e047-104">Use o procedimento a seguir para instalar o cliente do Microsoft Application Virtualization (App-V) 5,0 para que ele use o modo SCS (Shared Content Store) do App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3e047-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.0 client so that it uses the App-V 5.0 Shared Content Store (SCS) mode.</span></span> <span data-ttu-id="3e047-105">Você deve certificar-se de que todos os pré-requisitos necessários estejam instalados no computador para o qual você planeja instalar.</span><span class="sxs-lookup"><span data-stu-id="3e047-105">You should ensure that all required prerequisites are installed on the computer you plan to install to.</span></span> <span data-ttu-id="3e047-106">Use o link a seguir para os [pré-requisitos do App-V 5,0](app-v-50-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="3e047-106">Use the following link for a [App-V 5.0 Prerequisites](app-v-50-prerequisites.md).</span></span>

<span data-ttu-id="3e047-107">**Observação**  Antes de executar este procedimento, se necessário, desinstale qualquer versão existente do cliente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3e047-107">**Note** Before performing this procedure if necessary uninstall any existing version of the App-V 5.0 client.</span></span>

 

<span data-ttu-id="3e047-108">Para obter mais informações sobre o modo SCS, consulte [repositório de conteúdo compartilhado no Microsoft App-V 5,0 – por trás dos bastidores](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .</span><span class="sxs-lookup"><span data-stu-id="3e047-108">For more information about SCS mode, see [Shared Content Store in Microsoft App-V 5.0 – Behind the Scenes](https://go.microsoft.com/fwlink/?LinkId=316879) (https://go.microsoft.com/fwlink/?LinkId=316879).</span></span>

**<span data-ttu-id="3e047-109">Instalar e configurar o cliente do App-V 5,0 para o modo SCS</span><span class="sxs-lookup"><span data-stu-id="3e047-109">Install and configure the App-V 5.0 client for SCS mode</span></span>**

1.  <span data-ttu-id="3e047-110">Copie os arquivos de instalação do cliente do App-V 5,0 para o computador em que ele será instalado.</span><span class="sxs-lookup"><span data-stu-id="3e047-110">Copy the App-V 5.0 client installation files to the computer on which it will be installed.</span></span> <span data-ttu-id="3e047-111">Abra uma linha de comando e do diretório em que os arquivos de instalação são salvos digite uma das opções a seguir, dependendo da versão do cliente que você está instalando:</span><span class="sxs-lookup"><span data-stu-id="3e047-111">Open a command line and from the directory where the installation files are saved type one of the following options depending on the version of the client you are installing:</span></span>

    -   <span data-ttu-id="3e047-112">Para instalar a versão RDS do tipo de cliente App-V 5,0: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="3e047-112">To install the RDS version of the App-V 5.0 client type: **appv\_client\_setup\_rds.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

    -   <span data-ttu-id="3e047-113">Para instalar a versão padrão do tipo de cliente App-V 5,0: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**</span><span class="sxs-lookup"><span data-stu-id="3e047-113">To install the standard version of the App-V 5.0 client type: **appv\_client\_setup.exe /SHAREDCONTENTSTOREMODE=1 /q**</span></span>

        <span data-ttu-id="3e047-114">**Importante**  Você deve executar uma instalação silenciosa ou haverá falha na instalação.</span><span class="sxs-lookup"><span data-stu-id="3e047-114">**Important** You must perform a silent installation or the installation will fail.</span></span>

         

2.  <span data-ttu-id="3e047-115">Depois de concluir a instalação, você pode implantar pacotes no computador que está executando o cliente e todo o conteúdo do pacote será transmitido na rede.</span><span class="sxs-lookup"><span data-stu-id="3e047-115">After you have completed the installation you can deploy packages to the computer running the client and all package contents will be streamed across the network.</span></span>

    <span data-ttu-id="3e047-116">**Tem uma sugestão para o App-V**?</span><span class="sxs-lookup"><span data-stu-id="3e047-116">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="3e047-117">Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="3e047-117">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="3e047-118">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="3e047-118">Got an App-V issue?</span></span>** <span data-ttu-id="3e047-119">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="3e047-119">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="3e047-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e047-120">Related topics</span></span>


[<span data-ttu-id="3e047-121">Implantação do sequenciador e do cliente App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3e047-121">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





