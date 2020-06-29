---
title: Como implantar o cliente do MBAM em computadores desktop ou notebooks
description: Como implantar o cliente do MBAM em computadores desktop ou notebooks
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799693"
---
# <span data-ttu-id="bcecf-103">Como implantar o cliente do MBAM em computadores desktop ou notebooks</span><span class="sxs-lookup"><span data-stu-id="bcecf-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="bcecf-104">O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa.</span><span class="sxs-lookup"><span data-stu-id="bcecf-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="bcecf-105">O cliente MBAM pode ser integrado a uma organização ao implantar o cliente através de ferramentas, como os serviços de domínio Active Directory ou uma ferramenta de implantação de software empresarial, como o MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="bcecf-105">The MBAM Client can be integrated into an organization by deploying the client through tools, such as Active Directory Domain Services or an enterprise software deployment tool such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

<span data-ttu-id="bcecf-106">**Observação**  Para verificar os requisitos do sistema do cliente do MBAM, consulte [configurações compatíveis do MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="bcecf-106">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

**<span data-ttu-id="bcecf-107">Para implantar o cliente do MBAM em computadores desktop ou laptop</span><span class="sxs-lookup"><span data-stu-id="bcecf-107">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="bcecf-108">Localize os arquivos de instalação do cliente do MBAM fornecidos com o software do MBAM.</span><span class="sxs-lookup"><span data-stu-id="bcecf-108">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="bcecf-109">Implante o pacote do Windows Installer em computadores de destino usando os serviços de domínio Active Directory ou uma ferramenta de implantação de software corporativo, como MicrosoftSystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="bcecf-109">Deploy the Windows Installer package to target computers by using Active Directory Domain Services or an enterprise software deployment tool, such as MicrosoftSystemCenter2012 ConfigurationManager.</span></span>

    <span data-ttu-id="bcecf-110">**Observação**  Você não deve usar a política de grupo para implantar o pacote do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bcecf-110">**Note** You should not use Group Policy to deploy the Windows Installer package.</span></span>

     

3.  <span data-ttu-id="bcecf-111">Configurar as configurações de distribuição ou a política de grupo para executar o arquivo de instalação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="bcecf-111">Configure the distribution settings or Group Policy to run the MBAM Client installation file.</span></span> <span data-ttu-id="bcecf-112">Após a instalação bem-sucedida, o cliente MBAM aplica as configurações de política de grupo que são recebidas de um controlador de domínio para iniciar as funções de gerenciamento e criptografia do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bcecf-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker encryption and management functions.</span></span> <span data-ttu-id="bcecf-113">Para obter mais informações sobre configurações de política de grupo do MBAM, consulte [planejando requisitos de política de grupo do MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bcecf-113">For more information about MBAM Group Policy settings, see [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

    <span data-ttu-id="bcecf-114">**Importante**  O cliente MBAM não iniciará as ações de criptografia BitLocker se uma conexão de protocolo de área de trabalho remota estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="bcecf-114">**Important** The MBAM Client will not start BitLocker encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="bcecf-115">Todas as conexões de console remoto devem ser fechadas antes que a criptografia do BitLocker seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="bcecf-115">All remote console connections must be closed before BitLocker encryption will begin.</span></span>

     

## <span data-ttu-id="bcecf-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcecf-116">Related topics</span></span>


[<span data-ttu-id="bcecf-117">Implantando o Cliente do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="bcecf-117">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





