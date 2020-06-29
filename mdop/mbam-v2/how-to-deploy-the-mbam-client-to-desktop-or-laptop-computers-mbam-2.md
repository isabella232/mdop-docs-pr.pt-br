---
title: Como implantar o cliente do MBAM em computadores desktop ou notebooks
description: Como implantar o cliente do MBAM em computadores desktop ou notebooks
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796142"
---
# <span data-ttu-id="fa1b1-103">Como implantar o cliente do MBAM em computadores desktop ou notebooks</span><span class="sxs-lookup"><span data-stu-id="fa1b1-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="fa1b1-104">O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="fa1b1-104">The Microsoft BitLocker Administration and Monitoring (MBAM) client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="fa1b1-105">O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software eletrônico, como os serviços de domínio Active Directory ou o MicrosoftSystemCenterConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="fa1b1-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfigurationManager.</span></span>

<span data-ttu-id="fa1b1-106">**Observação**  Para verificar os requisitos do sistema do cliente de administração e administração do Microsoft BitLocker, consulte [configurações compatíveis do MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="fa1b1-106">**Note** To review the Microsoft BitLocker Administration and Monitoring Client system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

 

**<span data-ttu-id="fa1b1-107">Para implantar o cliente do MBAM em computadores desktop ou laptop</span><span class="sxs-lookup"><span data-stu-id="fa1b1-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="fa1b1-108">Localize os arquivos de instalação do cliente do MBAM fornecidos com o software do MBAM.</span><span class="sxs-lookup"><span data-stu-id="fa1b1-108">Locate the MBAM client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="fa1b1-109">Use os serviços de domínio do Active Directory ou uma ferramenta de implantação de software corporativo como o MicrosoftSystemCenterConfigurationManager para implantar o pacote do Windows Installer nos computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="fa1b1-109">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfigurationManager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="fa1b1-110">Configurar as configurações de distribuição ou a política de grupo para executar o arquivo de instalação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="fa1b1-110">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="fa1b1-111">Após a instalação bem-sucedida, o cliente MBAM aplica as configurações de política de grupo que são recebidas de um controlador de domínio para iniciar as funções de gerenciamento e criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fa1b1-111">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="fa1b1-112">Para obter mais informações sobre configurações de política de grupo do MBAM, consulte [planejando requisitos de política de grupo do MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="fa1b1-112">For more information about MBAM group policy settings, see [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md).</span></span>

    <span data-ttu-id="fa1b1-113">**Importante**  O cliente MBAM não iniciará as ações de criptografia BitLocker se uma conexão de protocolo de área de trabalho remota estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="fa1b1-113">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="fa1b1-114">Todas as conexões de console remoto devem ser fechadas antes que a criptografia do BitLocker seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="fa1b1-114">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="fa1b1-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa1b1-115">Related topics</span></span>


[<span data-ttu-id="fa1b1-116">Implantando o Cliente do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="fa1b1-116">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





