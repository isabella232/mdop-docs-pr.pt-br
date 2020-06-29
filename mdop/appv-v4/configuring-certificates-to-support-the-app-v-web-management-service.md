---
title: Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V
description: Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798015"
---
# <span data-ttu-id="c2ba4-103">Configuração de certificados para dar suporte ao Serviço de Gerenciamento da Web do App-V</span><span class="sxs-lookup"><span data-stu-id="c2ba4-103">Configuring Certificates to Support the App-V Web Management Service</span></span>


<span data-ttu-id="c2ba4-104">O serviço de gerenciamento da Web App-V deve ser configurado para dar suporte a conexões baseadas em SSL para ajudar a proteger a comunicação.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-104">The App-V Web Management Service must be configured to support SSL-based connections to help secure the communication.</span></span> <span data-ttu-id="c2ba4-105">Esse processo requer que o servidor Web ou computador no qual o serviço de gerenciamento está instalado tenha um certificado emitido para o serviço ou computador.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-105">This process requires that the Web server or computer on which the Management Service is installed has a certificate issued to the service or computer.</span></span>

<span data-ttu-id="c2ba4-106">Os cenários a seguir ilustram como obter um certificado para essa finalidade:</span><span class="sxs-lookup"><span data-stu-id="c2ba4-106">The following scenarios illustrate how to obtain a certificate for this purpose:</span></span>

1.  <span data-ttu-id="c2ba4-107">A infraestrutura da empresa já tem uma infraestrutura de chave pública (PKI) que emite certificados automaticamente para computadores.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-107">The company infrastructure already has a public key infrastructure (PKI) in place that automatically issues certificates to computers.</span></span>

2.  <span data-ttu-id="c2ba4-108">A infraestrutura da empresa já tem uma PKI in-loco, embora não emita certificados automaticamente para computadores.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-108">The company infrastructure already has a PKI in place, although it does not automatically issue certificates to computers.</span></span>

3.  <span data-ttu-id="c2ba4-109">A infraestrutura da empresa não tem PKI in-loco.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-109">The company infrastructure has no PKI in place.</span></span>

<span data-ttu-id="c2ba4-110">Em cada um dos cenários anteriores, o método para obter um certificado é diferente, mas o resultado final é o mesmo.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-110">In each of the preceding scenarios, the method for obtaining a certificate is different, but the end result is the same.</span></span> <span data-ttu-id="c2ba4-111">O administrador deve atribuir um certificado ao site padrão do IIS e configurar o serviço de gerenciamento da Web do App-V para exigir comunicações seguras.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-111">The administrator must assign a certificate to the IIS Default Web Site and configure the App-V Web Management Service to require secure communications.</span></span>

<span data-ttu-id="c2ba4-112">**Importante**  O nome do certificado deve corresponder ao nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-112">**Important** The name of the certificate must match the name of the server.</span></span> <span data-ttu-id="c2ba4-113">É uma prática recomendada usar nomes de domínio totalmente qualificados (FQDNs) para o nome comum do certificado.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-113">It is a best practice to use fully qualified domain names (FQDNs) for the common name of the certificate.</span></span>

 

<span data-ttu-id="c2ba4-114">O App-V pode usar os servidores IIS para dar suporte a diferentes configurações de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="c2ba4-114">App-V can use IIS servers to support different infrastructure configurations.</span></span> <span data-ttu-id="c2ba4-115">Para obter mais informações sobre a configuração de servidores IIS para suporte a HTTPS, consulte <https://go.microsoft.com/fwlink/?LinkId=151972> .</span><span class="sxs-lookup"><span data-stu-id="c2ba4-115">For more information about configuring IIS servers to support HTTPS, see <https://go.microsoft.com/fwlink/?LinkId=151972>.</span></span>

## <span data-ttu-id="c2ba4-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2ba4-116">Related topics</span></span>


[<span data-ttu-id="c2ba4-117">Como instalar e configurar o Console de Gerenciamento do App-V para um ambiente mais seguro</span><span class="sxs-lookup"><span data-stu-id="c2ba4-117">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





