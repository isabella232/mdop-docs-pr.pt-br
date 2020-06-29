---
title: Configurar os pré-requisitos do ambiente
description: Configurar os pré-requisitos do ambiente
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799874"
---
# <span data-ttu-id="21e6b-103">Configurar os pré-requisitos do ambiente</span><span class="sxs-lookup"><span data-stu-id="21e6b-103">Configure Environment Prerequisites</span></span>


<span data-ttu-id="21e6b-104">Antes de poder implantar e executar o Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, você deve garantir que seu ambiente atenda aos seguintes pré-requisitos mínimos.</span><span class="sxs-lookup"><span data-stu-id="21e6b-104">Before you can deploy and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you must ensure that your environment meets the following minimum prerequisites.</span></span>

**<span data-ttu-id="21e6b-105">Windows 7</span><span class="sxs-lookup"><span data-stu-id="21e6b-105">Windows 7</span></span>**

<span data-ttu-id="21e6b-106">O agente de host do MED-V e o pacote de espaço de trabalho do MED-V só têm suporte no Windows 7 ou versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="21e6b-106">The MED-V Host Agent and the MED-V Workspace Packager are only supported in Windows 7 or newer.</span></span>

**<span data-ttu-id="21e6b-107">Windows XP SP3</span><span class="sxs-lookup"><span data-stu-id="21e6b-107">Windows XP SP3</span></span>**

<span data-ttu-id="21e6b-108">O agente de convidado do MED-V só tem suporte no Windows XP SP3.</span><span class="sxs-lookup"><span data-stu-id="21e6b-108">The MED-V Guest Agent is only supported in Windows XP SP3.</span></span>

**<span data-ttu-id="21e6b-109">.NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="21e6b-109">.NET Framework 3.5 SP1</span></span>**

<span data-ttu-id="21e6b-110">O host do MED-V e os agentes convidados e o pacote do espaço de trabalho do MED-V exigem o Microsoft .NET Framework 3,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="21e6b-110">The MED-V Host and Guest agents and the MED-V Workspace Packager require the Microsoft .NET Framework 3.5 SP1.</span></span>

<span data-ttu-id="21e6b-111">**Importante**  Você também deve instalar a atualização [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) , que aborda vários problemas conhecidos de compatibilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21e6b-111">**Important** You must also install the update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950), which addresses several known application compatibility issues.</span></span>

 

<span data-ttu-id="21e6b-112">**Observação**  Você deve instalar manualmente o .NET Framework 3,5 SP1 e o Update KB959209 na imagem do PC virtual do Windows que você prepara para usar com o MED-V.</span><span class="sxs-lookup"><span data-stu-id="21e6b-112">**Note** You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="21e6b-113">No entanto, por padrão, o Microsoft .NET Framework 3,5 SP1 e a atualização são incluídos quando você instala o Windows 7 no computador host.</span><span class="sxs-lookup"><span data-stu-id="21e6b-113">However, by default, the Microsoft .NET Framework 3.5 SP1 and the update are included when you install Windows 7 on the host computer.</span></span>

 

**<span data-ttu-id="21e6b-114">Uma infra-estrutura do Active Directory</span><span class="sxs-lookup"><span data-stu-id="21e6b-114">An Active Directory Infrastructure</span></span>**

<span data-ttu-id="21e6b-115">A política de grupo fornece o gerenciamento centralizado e a configuração de sistemas operacionais, aplicativos e configurações dos usuários em um ambiente do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="21e6b-115">Group Policy provides the centralized management and configuration of operating systems, applications, and users' settings in an Active Directory environment.</span></span>

## <span data-ttu-id="21e6b-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="21e6b-116">Related topics</span></span>


[<span data-ttu-id="21e6b-117">Configurar os pré-requisitos de instalação</span><span class="sxs-lookup"><span data-stu-id="21e6b-117">Configure Installation Prerequisites</span></span>](configure-installation-prerequisites.md)

[<span data-ttu-id="21e6b-118">Arquitetura de alto nível</span><span class="sxs-lookup"><span data-stu-id="21e6b-118">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="21e6b-119">Configurações com suporte na MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="21e6b-119">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





