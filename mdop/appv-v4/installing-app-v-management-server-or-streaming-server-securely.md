---
title: Como instalar um servidor de gerenciamento do App-V ou um servidor de streaming com segurança
description: Como instalar um servidor de gerenciamento do App-V ou um servidor de streaming com segurança
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796903"
---
# <span data-ttu-id="1d36d-103">Como instalar um servidor de gerenciamento do App-V ou um servidor de streaming com segurança</span><span class="sxs-lookup"><span data-stu-id="1d36d-103">Installing App-V Management Server or Streaming Server Securely</span></span>


<span data-ttu-id="1d36d-104">Os tópicos desta seção fornecem informações para instalar uma versão de segurança aprimorada do servidor de gerenciamento do App-V ou do servidor de streaming do App-V.</span><span class="sxs-lookup"><span data-stu-id="1d36d-104">The topics in this section provide information for installing an enhanced security version of the App-V Management Server or the App-V Streaming Server.</span></span>

<span data-ttu-id="1d36d-105">**Observação**  A instalação ou configuração de um servidor de fluxo ou de gerenciamento do App-V para usar a segurança aprimorada (por exemplo, Transport Layer Security ou TLS) requer que um certificado X. 509 v3 seja provisionado para o App-V Server.</span><span class="sxs-lookup"><span data-stu-id="1d36d-105">**Note** Installing or configuring an App-V Management or Streaming Server to use enhanced security (for example, Transport Layer Security, or TLS) requires that an X.509 V3 certificate has been provisioned to the App-V server.</span></span>

 

<span data-ttu-id="1d36d-106">Ao se preparar para instalar ou configurar um servidor de fluxo e gerenciamento seguro, considere os seguintes requisitos técnicos:</span><span class="sxs-lookup"><span data-stu-id="1d36d-106">When you prepare to install or configure a secure Management or Streaming Server, consider the following technical requirements:</span></span>

-   <span data-ttu-id="1d36d-107">O certificado deve ser válido.</span><span class="sxs-lookup"><span data-stu-id="1d36d-107">The certificate must be valid.</span></span> <span data-ttu-id="1d36d-108">Se o certificado não for válido, o cliente encerrará a conexão.</span><span class="sxs-lookup"><span data-stu-id="1d36d-108">If the certificate is not valid, the client ends the connection.</span></span>

-   <span data-ttu-id="1d36d-109">O certificado deve conter o *uso de chave avançada* (EKU) correto, autenticação do servidor (OID 1.3.6.1.5.5.7.3.1).</span><span class="sxs-lookup"><span data-stu-id="1d36d-109">The certificate must contain the correct *Enhanced Key Usage* (EKU)—Server Authentication (OID 1.3.6.1.5.5.7.3.1).</span></span> <span data-ttu-id="1d36d-110">Se o certificado não contiver esse EKU, o cliente encerrará a conexão.</span><span class="sxs-lookup"><span data-stu-id="1d36d-110">If the certificate does not contain this EKU, the client ends the connection.</span></span>

-   <span data-ttu-id="1d36d-111">O nome de domínio totalmente qualificado (FQDN) do certificado deve corresponder ao servidor no qual ele está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d36d-111">The certificate fully qualified domain name (FQDN) must match the server on which it is installed.</span></span> <span data-ttu-id="1d36d-112">Por exemplo, se o cliente estiver chamando `RTSPS://Myserver.mycompany.com/content/MyApp.sft` e o campo certificado **emitido para** está definido como `Server1.mycompany.com` , o cliente não se conectará ao servidor e a sessão será encerrada.</span><span class="sxs-lookup"><span data-stu-id="1d36d-112">For example, if the client is calling `RTSPS://Myserver.mycompany.com/content/MyApp.sft` and the certificate **Issued To** field is set to `Server1.mycompany.com`, the client will not connect to the server and the session ends.</span></span> <span data-ttu-id="1d36d-113">A falha é reportada para o usuário.</span><span class="sxs-lookup"><span data-stu-id="1d36d-113">The failure is reported to the user.</span></span>

    <span data-ttu-id="1d36d-114">**Observação**  Se você estiver usando o App-V em um cluster de balanceamento de carga de rede, será preciso configurar o certificado com nomes alternativos de assunto (SANs) para dar suporte a RTSPs.</span><span class="sxs-lookup"><span data-stu-id="1d36d-114">**Note** If you are using App-V in a Network Load Balancing cluster, you must configure the certificate with Subject Alternate Names (SANs) to support RTSPS.</span></span> <span data-ttu-id="1d36d-115">Para obter informações sobre como configurar a CA (autoridade de certificação) e criar certificados com SANs, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="1d36d-115">For information about configuring the certification authority (CA) and creating certificates with SANs, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

     

-   <span data-ttu-id="1d36d-116">O cliente e o servidor precisam confiar na CA raiz – a autoridade de certificação que emite o certificado para o servidor App-V deve ser confiável para o cliente se conectando ao servidor.</span><span class="sxs-lookup"><span data-stu-id="1d36d-116">The client and the server need to trust the root CA—The CA issuing the certificate to the App-V server must by trusted by the client connecting to the server.</span></span> <span data-ttu-id="1d36d-117">Caso contrário, o cliente finalizará a conexão.</span><span class="sxs-lookup"><span data-stu-id="1d36d-117">If not, the client ends the connection.</span></span>

-   <span data-ttu-id="1d36d-118">A chave privada do certificado deve ter permissões alteradas para permitir que a conta de serviço do App-V acesse o certificado.</span><span class="sxs-lookup"><span data-stu-id="1d36d-118">The certificate’s private key must have permissions changed to allow the App-V Service account to access the certificate.</span></span> <span data-ttu-id="1d36d-119">Por padrão, o App-V usa a conta de serviço de rede e, por padrão, a conta de serviço de rede não tem permissão para acessar a chave privada, o que impedirá conexões seguras.</span><span class="sxs-lookup"><span data-stu-id="1d36d-119">By default, App-V uses the Network Service account, and by default, the Network Service account does not have permission to access the private key, which will prevent secure connections.</span></span>

## <span data-ttu-id="1d36d-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1d36d-120">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[<span data-ttu-id="1d36d-121">Configuração de certificados para dar suporte ao streaming seguro</span><span class="sxs-lookup"><span data-stu-id="1d36d-121">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)  
<span data-ttu-id="1d36d-122">Fornece informações sobre como obter, configurar e instalar certificados para dar suporte ao streaming seguro.</span><span class="sxs-lookup"><span data-stu-id="1d36d-122">Provides information about obtaining, configuring, and installing certificates to support secure streaming.</span></span>

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[<span data-ttu-id="1d36d-123">Como modificar permissões de chave privada para dar suporte ao servidor de gerenciamento ou ao servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="1d36d-123">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
<span data-ttu-id="1d36d-124">Fornece procedimentos que você pode usar para modificar as chaves no Windows Server2003 e no Windows Server2008.</span><span class="sxs-lookup"><span data-stu-id="1d36d-124">Provides procedures you can use to modify keys in Windows Server2003 and Windows Server2008.</span></span>

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[<span data-ttu-id="1d36d-125">Configuração de certificados para dar suporte ao servidor de gerenciamento ou ao servidor de streaming do App-V</span><span class="sxs-lookup"><span data-stu-id="1d36d-125">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
<span data-ttu-id="1d36d-126">Fornece informações sobre como configurar certificados para os servidores de gerenciamento ou de fluxo do App-V, incluindo informações sobre como configurar certificados para ambientes de balanceamento de carga de rede.</span><span class="sxs-lookup"><span data-stu-id="1d36d-126">Provides information about configuring certificates for the App-V Management or Streaming Servers, including information about configuring certificates for Network Load Balancing environments.</span></span>

 

 





