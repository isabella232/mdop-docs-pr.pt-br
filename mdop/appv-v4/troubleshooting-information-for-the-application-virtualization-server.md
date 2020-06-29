---
title: Informações para solução de problemas do Application Virtualization Server
description: Informações para solução de problemas do Application Virtualization Server
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796675"
---
# <span data-ttu-id="5bd02-103">Informações para solução de problemas do Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="5bd02-103">Troubleshooting Information for the Application Virtualization Server</span></span>


<span data-ttu-id="5bd02-104">Este tópico inclui informações que você pode usar para solucionar vários problemas nos servidores do Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="5bd02-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Servers.</span></span>

## <span data-ttu-id="5bd02-105">Mensagem de aviso 25017 no log de instalação após a instalação do servidor</span><span class="sxs-lookup"><span data-stu-id="5bd02-105">Warning Message 25017 in Setup Log After Installing the Server</span></span>


<span data-ttu-id="5bd02-106">Você pode encontrar a seguinte mensagem no log de instalação do servidor após a instalação.</span><span class="sxs-lookup"><span data-stu-id="5bd02-106">You might find the following message in the server setup log after installation.</span></span>

*<span data-ttu-id="5bd02-107">Aviso 25017.</span><span class="sxs-lookup"><span data-stu-id="5bd02-107">Warning 25017.</span></span> <span data-ttu-id="5bd02-108">O programa de instalação não pôde criar o objeto do marcador do Active Directory para o servidor.</span><span class="sxs-lookup"><span data-stu-id="5bd02-108">The installation Program could not create the Active Directory marker object for the server.</span></span> <span data-ttu-id="5bd02-109">A conta usada para instalar não tinha os direitos suficientes para gravar no Active Directory ou o Active Directory estava indisponível.</span><span class="sxs-lookup"><span data-stu-id="5bd02-109">The account used to install did not have the sufficient rights to write to Active Directory or Active Directory was unavailable.</span></span>*

<span data-ttu-id="5bd02-110">O instalador do App-V ou o instalador do Stream Server cria uma entrada de ponto de conexão de serviço no objeto de computador nos serviços de domínio Active Directory (ADDS) que corresponde ao computador no qual o servidor está instalado se a conta usada para executar o instalador tem os direitos apropriados.</span><span class="sxs-lookup"><span data-stu-id="5bd02-110">The App-V Management or Streaming Server installer creates a Service Connection Point entry under the Computer object in Active Directory Domain Services (ADDS) that corresponds to the computer on which the server is installed if the account used to run the installer has the appropriate rights.</span></span> <span data-ttu-id="5bd02-111">Não criar essa entrada não fará com que a instalação falhe, e isso não afetará o funcionamento do produto.</span><span class="sxs-lookup"><span data-stu-id="5bd02-111">Failure to create this entry will not cause the install to fail and this should not otherwise affect the functioning of the product.</span></span> <span data-ttu-id="5bd02-112">A causa mais provável de qualquer falha é que a conta de usuário usada para executar a instalação não tinha direitos suficientes para gravar em adições.</span><span class="sxs-lookup"><span data-stu-id="5bd02-112">The likely cause of any failure is that the user account used to run the install did not have sufficient rights to write to ADDS.</span></span> <span data-ttu-id="5bd02-113">Embora o registro do App-V Server no ADDS seja opcional, um benefício disso permite que as ferramentas de gerenciamento centralizado localizem o servidor App-V para fins de inventário e gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="5bd02-113">Although registering the App-V server in ADDS is optional, one benefit of doing so enables centralized management tools to locate the App-V server for inventory and management purposes.</span></span>

## <span data-ttu-id="5bd02-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bd02-114">Related topics</span></span>


[<span data-ttu-id="5bd02-115">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="5bd02-115">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





