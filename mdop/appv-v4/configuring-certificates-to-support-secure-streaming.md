---
title: Configuração de certificados para dar suporte ao streaming seguro
description: Configuração de certificados para dar suporte ao streaming seguro
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798016"
---
# <span data-ttu-id="9bcdd-103">Configuração de certificados para dar suporte ao streaming seguro</span><span class="sxs-lookup"><span data-stu-id="9bcdd-103">Configuring Certificates to Support Secure Streaming</span></span>


<span data-ttu-id="9bcdd-104">Por padrão, o serviço App-V é executado na conta de serviço de rede.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-104">By default, the App-V service runs under the Network Service account.</span></span> <span data-ttu-id="9bcdd-105">No entanto, você pode criar uma conta de serviço nos serviços de domínio Active Directory e substituir a conta de serviço de rede pela conta de domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-105">However, you can create a service account in Active Directory Domain Services and replace the Network Service account with the Active Directory Domain account.</span></span>

<span data-ttu-id="9bcdd-106">O contexto de segurança no qual o serviço é executado é importante para configurar comunicações seguras aprimoradas.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-106">The security context under which the service runs is important for configuring enhanced secure communications.</span></span> <span data-ttu-id="9bcdd-107">Esse contexto de segurança deve ter permissões de leitura para a chave privada do certificado.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-107">This security context must have read permissions for the certificate private key.</span></span> <span data-ttu-id="9bcdd-108">Quando um arquivo PKCS \ #10 *solicitação de assinatura de certificado* (CSR) é gerado para o servidor App-V, o provedor de serviços de *criptografia* do Windows é chamado e uma chave privada é gerada.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-108">When a PKCS\#10 *Certificate Signing Request* (CSR) is generated for the App-V server, the Windows *Cryptographic Service Provider* is called and a private key is generated.</span></span> <span data-ttu-id="9bcdd-109">A chave privada é protegida com permissões dadas apenas às contas de sistema e administrador.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-109">The private key is secured with permissions given to the System and Administrator accounts only.</span></span>

<span data-ttu-id="9bcdd-110">Você deve modificar as listas de controle de acesso (ACLs) na chave privada para permitir que o gerenciamento do App-V ou o Streaming Server acessem a chave privada necessária para comunicações seguras protegidas de TLS.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-110">You must modify the access control lists (ACLs) on the private key to let the App-V Management or Streaming Server access the private key required for successful TLS secured communication.</span></span>

## <span data-ttu-id="9bcdd-111">Obtendo e instalando um certificado</span><span class="sxs-lookup"><span data-stu-id="9bcdd-111">Obtaining and Installing a Certificate</span></span>


<span data-ttu-id="9bcdd-112">Os cenários para obter e instalar um certificado para o App-V são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="9bcdd-112">The scenarios for obtaining and installing a certificate for App-V are as follows:</span></span>

-   <span data-ttu-id="9bcdd-113">Infraestrutura de chave pública interna (PKI).</span><span class="sxs-lookup"><span data-stu-id="9bcdd-113">Internal public key infrastructure (PKI).</span></span>

-   <span data-ttu-id="9bcdd-114">Autoridade de certificação (CA) de emissão de certificados terceirizada.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-114">Third-party certificate issuing certification authority (CA).</span></span>

    <span data-ttu-id="9bcdd-115">**Observação**  Se você precisar obter um certificado de uma autoridade de certificação terceirizada, siga a documentação disponível nesse site da Web da CA.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-115">**Note** If you need to obtain a certificate from a third-party CA, follow the documentation available on that CA’s Web site.</span></span>

     

<span data-ttu-id="9bcdd-116">Se uma infraestrutura de PKI foi implantada, consulte os administradores de PKI para adquirir um certificado compatível com os requisitos descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-116">If a PKI infrastructure has been deployed, consult with the PKI administrators to acquire a certificate that complies with the requirements described in this topic.</span></span> <span data-ttu-id="9bcdd-117">Se uma infraestrutura de PKI não estiver disponível, use uma CA de terceiros para obter um certificado válido.</span><span class="sxs-lookup"><span data-stu-id="9bcdd-117">If a PKI infrastructure is not available, use a third-party CA to obtain a valid certificate.</span></span>

<span data-ttu-id="9bcdd-118">Para obter orientação passo a passo para obter e instalar um certificado, consulte <https://go.microsoft.com/fwlink/?LinkId=151969> .</span><span class="sxs-lookup"><span data-stu-id="9bcdd-118">For step-by-step guidance for obtaining and installing a certificate, see <https://go.microsoft.com/fwlink/?LinkId=151969>.</span></span>

## <span data-ttu-id="9bcdd-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bcdd-119">Related topics</span></span>


<span data-ttu-id="9bcdd-120">Configurar certificados para dar suporte ao streaming seguro [como modificar as permissões de chave privada para o servidor de gerenciamento de suporte ou o Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span><span class="sxs-lookup"><span data-stu-id="9bcdd-120">Configuring Certificates to Support Secure Streaming [How to Modify Private Key Permissions to Support Management Server or Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)</span></span>

 

 





