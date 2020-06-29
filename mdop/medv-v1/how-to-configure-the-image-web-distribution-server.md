---
title: Como configurar o servidor de distribuição na Web de imagem
description: Como configurar o servidor de distribuição na Web de imagem
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799616"
---
# <span data-ttu-id="79d21-103">Como configurar o servidor de distribuição na Web de imagem</span><span class="sxs-lookup"><span data-stu-id="79d21-103">How to Configure the Image Web Distribution Server</span></span>


<span data-ttu-id="79d21-104">Um repositório de imagens é um servidor opcional que é usado para distribuição de imagens (em que os administradores carregam novas imagens e os computadores cliente verificam o servidor a cada 15 minutos e atualizam sua imagem se um novo estiver disponível).</span><span class="sxs-lookup"><span data-stu-id="79d21-104">An image repository is an optional server that is used for image distribution (where administrators upload new images and client computers check the server every 15 minutes and update their image if a new one is available).</span></span>

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


<span data-ttu-id="79d21-105">Um servidor de distribuição de imagens requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="79d21-105">An image distribution server requires the following:</span></span>

-   <span data-ttu-id="79d21-106">Serviços de informações da Internet (IIS) — para obter informações, consulte [serviços de informações da Internet](https://go.microsoft.com/fwlink/?LinkId=142995).</span><span class="sxs-lookup"><span data-stu-id="79d21-106">Internet Information Services (IIS)—For information, see [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span></span>

    <span data-ttu-id="79d21-107">Durante a instalação do IIS, ao adicionar serviços de função, selecione os seguintes métodos de autenticação compatíveis:</span><span class="sxs-lookup"><span data-stu-id="79d21-107">During the IIS installation, when adding role services, select the following supported authentication methods:</span></span>

    -   **<span data-ttu-id="79d21-108">Autenticação básica</span><span class="sxs-lookup"><span data-stu-id="79d21-108">Basic Authentication</span></span>**

    -   **<span data-ttu-id="79d21-109">Autenticação do Windows</span><span class="sxs-lookup"><span data-stu-id="79d21-109">Windows Authentication</span></span>**

    -   **<span data-ttu-id="79d21-110">Autenticação de mapeamento de certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="79d21-110">Client Certificate Mapping Authentication</span></span>**

    <span data-ttu-id="79d21-111">Ao configurar o IIS, inclua o seguinte:</span><span class="sxs-lookup"><span data-stu-id="79d21-111">When configuring IIS, include the following:</span></span>

    -   <span data-ttu-id="79d21-112">Adicione um diretório virtual, com o alias chamado **MEDVImages**.</span><span class="sxs-lookup"><span data-stu-id="79d21-112">Add a virtual directory, with the alias named **MEDVImages**.</span></span> <span data-ttu-id="79d21-113">O caminho físico deve apontar para o local das imagens.</span><span class="sxs-lookup"><span data-stu-id="79d21-113">The physical path should point to the location of the images.</span></span>

    -   <span data-ttu-id="79d21-114">Habilite o BITS.</span><span class="sxs-lookup"><span data-stu-id="79d21-114">Enable BITS.</span></span>

    -   <span data-ttu-id="79d21-115">Adicione os seguintes tipos de MIME:</span><span class="sxs-lookup"><span data-stu-id="79d21-115">Add the following MIME types:</span></span>

        -   **<span data-ttu-id="79d21-116">. CKM (application/octet-stream)</span><span class="sxs-lookup"><span data-stu-id="79d21-116">.ckm (application/octet-stream)</span></span>**

        -   <span data-ttu-id="79d21-117">**. Index (application/octet-stream**)</span><span class="sxs-lookup"><span data-stu-id="79d21-117">**.index (application/octet-stream**)</span></span>

    -   <span data-ttu-id="79d21-118">No site do MED-V, adicione permissões de leitura para **todos**.</span><span class="sxs-lookup"><span data-stu-id="79d21-118">On the MED-V site, add read permissions to **Everyone**.</span></span>

    -   <span data-ttu-id="79d21-119">Reinicie o IIS.</span><span class="sxs-lookup"><span data-stu-id="79d21-119">Restart IIS.</span></span>

-   <span data-ttu-id="79d21-120">Extensões de servidor BITS para IIS — para obter informações, consulte [instalar extensões de servidor bits](https://go.microsoft.com/fwlink/?LinkId=142996).</span><span class="sxs-lookup"><span data-stu-id="79d21-120">BITS Server Extensions for IIS—For information, see [Install BITS Server Extensions](https://go.microsoft.com/fwlink/?LinkId=142996).</span></span>

## <span data-ttu-id="79d21-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79d21-121">Related topics</span></span>


[<span data-ttu-id="79d21-122">Configurações com suporte</span><span class="sxs-lookup"><span data-stu-id="79d21-122">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="79d21-123">Projetar os repositórios de imagens do MED-V</span><span class="sxs-lookup"><span data-stu-id="79d21-123">Design the MED-V Image Repositories</span></span>](design-the-med-v-image-repositories.md)

 

 





