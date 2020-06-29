---
title: Como implantar o cliente do MBAM em computadores desktop ou notebooks
description: Como implantar o cliente do MBAM em computadores desktop ou notebooks
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799480"
---
# <span data-ttu-id="7bc50-103">Como implantar o cliente do MBAM em computadores desktop ou notebooks</span><span class="sxs-lookup"><span data-stu-id="7bc50-103">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="7bc50-104">Este tópico explica como implantar o cliente MBAM para os computadores dos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="7bc50-104">This topic explains how to deploy the MBAM Client to end users’ computers.</span></span> <span data-ttu-id="7bc50-105">Você pode implantar o cliente MBAM por meio de um sistema de distribuição de software eletrônico, como os serviços de domínio Active Directory ou o Gerenciador de MicrosoftSystemCenterConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7bc50-105">You can deploy the MBAM Client through an electronic software distribution system, such as Active Directory Domain Services or MicrosoftSystemCenterConfiguration Manager.</span></span>

<span data-ttu-id="7bc50-106">Para implantar o cliente MBAM como parte de uma implantação do Windows, consulte [como habilitar o BitLocker usando o MBAM como parte de uma implantação do Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="7bc50-106">To deploy the MBAM Client as part of a Windows deployment, see [How to Enable BitLocker by Using MBAM as Part of a Windows Deployment](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).</span></span>

<span data-ttu-id="7bc50-107">Antes de iniciar a implantação do cliente MBAM, examine as [configurações compatíveis do MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7bc50-107">Before you start the MBAM Client deployment, review the [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="7bc50-108">Para implantar o cliente do MBAM em computadores desktop ou laptop</span><span class="sxs-lookup"><span data-stu-id="7bc50-108">To deploy the MBAM Client to desktop or laptop computers</span></span>**

1.  <span data-ttu-id="7bc50-109">Localize os arquivos de instalação do cliente do MBAM fornecidos com o software do MBAM.</span><span class="sxs-lookup"><span data-stu-id="7bc50-109">Locate the MBAM Client installation files that are provided with the MBAM software.</span></span>

2.  <span data-ttu-id="7bc50-110">Use os serviços de domínio do Active Directory ou uma ferramenta de implantação de software corporativo, como o MicrosoftSystemCenterConfiguration Manager, para implantar o pacote do Windows Installer em computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="7bc50-110">Use Active Directory Domain Services or an enterprise software deployment tool like MicrosoftSystemCenterConfiguration Manager to deploy the Windows Installer package to target computers.</span></span>

3.  <span data-ttu-id="7bc50-111">Defina as configurações de distribuição ou as configurações de política de grupo para executar o arquivo de instalação do cliente MBAM.</span><span class="sxs-lookup"><span data-stu-id="7bc50-111">Configure the distribution settings or Group Policy settings to run the MBAM Client installation file.</span></span>

    <span data-ttu-id="7bc50-112">Após a instalação bem-sucedida, o cliente MBAM aplica as configurações de política de grupo que são recebidas de um controlador de domínio para iniciar as funções de gerenciamento e criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7bc50-112">After successful installation, the MBAM Client applies the Group Policy settings that are received from a domain controller to begin BitLocker Drive Encryption and management functions.</span></span>

    <span data-ttu-id="7bc50-113">**Importante**  O cliente MBAM não iniciará as ações de criptografia de unidade de disco BitLocker se uma conexão de protocolo de área de trabalho remota estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="7bc50-113">**Important** The MBAM Client does not start BitLocker Drive Encryption actions if a remote desktop protocol connection is active.</span></span> <span data-ttu-id="7bc50-114">Todas as conexões de console remoto devem ser fechadas e um usuário deve estar conectado a uma sessão de console físico antes do início da criptografia de unidade de disco BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7bc50-114">All remote console connections must be closed and a user must be logged on to a physical console session before BitLocker Drive Encryption begins.</span></span>

     


## <span data-ttu-id="7bc50-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bc50-115">Related topics</span></span>
[<span data-ttu-id="7bc50-116">Implantando o cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7bc50-116">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

[<span data-ttu-id="7bc50-117">Planejando a implantação do cliente do MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7bc50-117">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

 

## <span data-ttu-id="7bc50-118">Tem uma sugestão para o MBAM?</span><span class="sxs-lookup"><span data-stu-id="7bc50-118">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7bc50-119">Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="7bc50-119">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="7bc50-120">Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="7bc50-120">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





