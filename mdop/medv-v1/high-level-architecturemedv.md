---
title: Arquitetura de alto nível
description: Arquitetura de alto nível
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799825"
---
# <span data-ttu-id="fc10f-103">Arquitetura de alto nível</span><span class="sxs-lookup"><span data-stu-id="fc10f-103">High-Level Architecture</span></span>


<span data-ttu-id="fc10f-104">A solução MED-V inclui os seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="fc10f-104">The MED-V solution comprises the following elements:</span></span>

-   <span data-ttu-id="fc10f-105">**Máquina virtual definida pelo administrador**— encapsula um ambiente de área de trabalho completo, incluindo um sistema operacional, aplicativos e ferramentas de gerenciamento e segurança opcionais.</span><span class="sxs-lookup"><span data-stu-id="fc10f-105">**Administrator-defined virtual machine**—Encapsulates a full desktop environment, including an operating system, applications, and optional management and security tools.</span></span>

-   <span data-ttu-id="fc10f-106">**Repositório de imagens**— armazena todas as imagens virtuais em um servidor IIS padrão e habilita o gerenciamento de versão de imagens virtuais, a recuperação de imagens autenticadas pelo cliente e o download eficiente (de uma nova imagem ou atualizações) via tecnologia de transferência de corte.</span><span class="sxs-lookup"><span data-stu-id="fc10f-106">**Image repository**—Stores all virtual images on a standard IIS server and enables virtual images version management, client-authenticated image retrieval, and efficient download (of a new image or updates) via Trim Transfer technology.</span></span>

-   <span data-ttu-id="fc10f-107">**Servidor de gerenciamento**— associa imagens virtuais do repositório de imagens juntamente com as políticas de uso do administrador ao Active Directory® usuários ou grupos.</span><span class="sxs-lookup"><span data-stu-id="fc10f-107">**Management server**—Associates virtual images from the image repository along with administrator usage policies to Active Directory® users or groups.</span></span> <span data-ttu-id="fc10f-108">O servidor de gerenciamento também agrega eventos dos clientes e os armazena em um banco de dados externo (Microsoft SQL Server®) para fins de monitoramento e relatórios.</span><span class="sxs-lookup"><span data-stu-id="fc10f-108">The management server also aggregates clients' events and stores them in an external database (Microsoft SQL Server®) for monitoring and reporting purposes.</span></span>

-   <span data-ttu-id="fc10f-109">**Console de gerenciamento**— permite que os administradores controlem o servidor de gerenciamento e o repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="fc10f-109">**Management console**—Enables administrators to control the management server and the image repository.</span></span>

-   **<span data-ttu-id="fc10f-110">Cliente de usuário final</span><span class="sxs-lookup"><span data-stu-id="fc10f-110">End-user client</span></span>**

    1.  <span data-ttu-id="fc10f-111">Ciclo de vida da imagem virtual — autenticação, recuperação de imagens, imposição de políticas de uso.</span><span class="sxs-lookup"><span data-stu-id="fc10f-111">Virtual image life-cycle—Authentication, image retrieval, enforcement of usage policies.</span></span>

    2.  <span data-ttu-id="fc10f-112">Gerenciamento de sessões de máquinas virtuais — Iniciar, parar, bloquear a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc10f-112">Virtual machine session management—Start, stop, lock the virtual machine.</span></span>

    3.  <span data-ttu-id="fc10f-113">Experiência única na área de trabalho: os aplicativos instalados na máquina virtual diretamente disponíveis por meio do menu Iniciar da área de trabalho padrão e integrados a outros aplicativos na área de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc10f-113">Single desktop experience—Applications installed in the virtual machine seamlessly available through the standard desktop Start menu and integrated with other applications on the user desktop.</span></span>

<span data-ttu-id="fc10f-114">Toda a comunicação entre o cliente e os servidores (servidor de gerenciamento e o repositório de imagens) é realizada sobre um canal HTTP ou HTTPS padrão.</span><span class="sxs-lookup"><span data-stu-id="fc10f-114">All communication between the client and the servers (management server and image repository) is carried on top of a standard HTTP or HTTPS channel.</span></span>

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





