---
title: Visão geral de segurança e proteção
description: Visão geral de segurança e proteção
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796769"
---
# <span data-ttu-id="f5fc9-103">Visão geral de segurança e proteção</span><span class="sxs-lookup"><span data-stu-id="f5fc9-103">Security and Protection Overview</span></span>


<span data-ttu-id="f5fc9-104">O Microsoft Application Virtualization 4.5 oferece os seguintes recursos de segurança aprimorados para ajudar você a planejar e implementar uma estratégia de implantação mais segura:</span><span class="sxs-lookup"><span data-stu-id="f5fc9-104">Microsoft Application Virtualization4.5 provides the following enhanced security features to help you plan and implement a more secure deployment strategy:</span></span>

-   <span data-ttu-id="f5fc9-105">A virtualização de aplicativos agora oferece suporte a TLS (Transport Layer Security) usando certificados do X. 509 v3.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-105">Application Virtualization now supports Transport Layer Security (TLS) using X.509 V3 certificates.</span></span> <span data-ttu-id="f5fc9-106">Desde que um certificado do servidor tenha sido provisionado para o gerenciamento de aplicativo de aplicativos ou o servidor de streaming planejado, a instalação padrão será segura, usando o protocolo RTSP na porta 322.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-106">Provided that a server certificate has been provisioned to the planned Application Virtualization Management or Streaming Server, the installation will default to secure, using the RTSPS protocol over port 322.</span></span> <span data-ttu-id="f5fc9-107">Usar RTSPs garante que a comunicação entre os servidores de virtualização de aplicativos e os clientes de virtualização de aplicativos seja assinada e criptografada.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-107">Using RTSPS ensures that communication between the Application Virtualization Servers and the Application Virtualization Clients is signed and encrypted.</span></span> <span data-ttu-id="f5fc9-108">Se nenhum certificado for atribuído ao servidor durante a instalação do servidor do Application Virtualization, a comunicação será definida como RTSP na porta 554.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-108">If no certificate is assigned to the server during the Application Virtualization Server installation, the communication will be set to RTSP over port 554.</span></span>

    **<span data-ttu-id="f5fc9-109">Observação de segurança:</span><span class="sxs-lookup"><span data-stu-id="f5fc9-109">Security Note:</span></span>**

    <span data-ttu-id="f5fc9-110">Para ajudar a oferecer uma configuração de segurança do servidor, você deve verificar se as portas RTSP estão desativadas, mesmo que você tenha todos os pacotes configurados para usar RTSPs.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-110">To help provide a secure setup of the server, you must make sure that RTSP ports are disabled even if you have all packages configured to use RTSPS.</span></span>

    <span data-ttu-id="f5fc9-111">Se você adicionar certificados de segurança ao servidor após a instalação do servidor, o servidor talvez não detecte os certificados.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-111">If you add security certificates to the server after installing the server, the server might not detect the certificates.</span></span> <span data-ttu-id="f5fc9-112">Para ajudar a garantir a detecção do certificado de segurança, reinicie o servidor após adicionar os certificados.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-112">To help ensure security certificate detection, restart the server after adding the certificates.</span></span>

-   <span data-ttu-id="f5fc9-113">O cliente deve ser configurado para usar o mesmo protocolo e a mesma porta do servidor ou não poderá se comunicar com o servidor.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-113">The client must be configured to use the same protocol and port as the server, or it will not be able to communicate with the server.</span></span> <span data-ttu-id="f5fc9-114">O cliente também deve confiar no emissor do certificado e vem com vários dos provedores primários em seu armazenamento raiz confiável.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-114">The client must also trust the issuer of the certificate and ships with several of the primary providers in its Trusted Root Store.</span></span> <span data-ttu-id="f5fc9-115">Você pode usar certificados autoassinados, mas será necessário atualizar os clientes.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-115">You can use self-signed certificates, but you will need to update the clients.</span></span>

-   <span data-ttu-id="f5fc9-116">Ao configurar os servidores IIS para usar o protocolo HTTPS para streaming, você precisará configurar o Secure Sockets Layer (SSL) no servidor IIS e provisionar o certificado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-116">When configuring IIS servers to use the HTTPS protocol for streaming, you will need to set up Secure Sockets Layer (SSL) on the IIS server and provision the certificate for the server.</span></span> <span data-ttu-id="f5fc9-117">Além disso, os clientes precisarão ser configurados para confiar na autoridade de certificação raiz que emitiu o certificado do servidor.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-117">The clients will also need to be configured to trust the root certification authority that issued the server certificate.</span></span>

-   <span data-ttu-id="f5fc9-118">A autenticação Kerberos foi adicionada ao Microsoft Application Virtualization como o mecanismo de autenticação padrão.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-118">Kerberos authentication has been added to Microsoft Application Virtualization as the default authentication mechanism.</span></span> <span data-ttu-id="f5fc9-119">Versões anteriores dependentes do NTLM v2 para autenticação.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-119">Earlier versions relied upon NTLM V2 for authentication.</span></span> <span data-ttu-id="f5fc9-120">Usar a autenticação Kerberos reforça a segurança da comunicação entre o cliente e o servidor do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-120">Using Kerberos Authentication strengthens the security of the communication between the client and the Application Virtualization server.</span></span> <span data-ttu-id="f5fc9-121">Quando uma conexão é iniciada do cliente, o servidor de virtualização de aplicativos verifica a permissão de sessão com o centro de distribuição de chaves (KDC).</span><span class="sxs-lookup"><span data-stu-id="f5fc9-121">When a connection has been initiated from the client, the Application Virtualization Server verifies the session ticket with the Key Distribution Center (KDC).</span></span>

-   <span data-ttu-id="f5fc9-122">Devido ao suporte para o uso de certificados de servidor e o uso de protocolos HTTPS ou HTTPS, agora você pode oferecer suporte a clientes fora da rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-122">Because of the support for using server certificates and using the RTSPS or HTTPS protocols, you can now support clients outside of the corporate network.</span></span> <span data-ttu-id="f5fc9-123">Isso pode ajudar a eliminar a necessidade de usuários móveis de configurar uma conexão segura com a rede corporativa (VPN, RAS e assim por diante) antes de iniciar aplicativos provisionados do Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-123">This can help eliminate the need for mobile users to set up a secure connection to the corporate network (VPN, RAS, and so on) prior to launching Application Virtualization provisioned applications.</span></span>

<span data-ttu-id="f5fc9-124">Outras importantes considerações de segurança a serem consideradas incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f5fc9-124">Other important security considerations to consider include the following:</span></span>

-   <span data-ttu-id="f5fc9-125">Sempre mantenha os servidores totalmente atualizados e protegidos.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-125">Always keep servers fully updated and protected.</span></span>

-   <span data-ttu-id="f5fc9-126">Para adicionar um certificado para permitir comunicações mais seguras com o servidor de gerenciamento do Application Virtualization, os seguintes critérios devem ser atendidos:</span><span class="sxs-lookup"><span data-stu-id="f5fc9-126">To add a certificate to enable more secure communications to the Application Virtualization Management Server, the following criteria must be met:</span></span>

    -   <span data-ttu-id="f5fc9-127">O usuário que adicionará o certificado deve ser um administrador no servidor em que o repositório de certificados está localizado.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-127">The user who will be adding the certificate must be an administrator on the server where the certificate store is located.</span></span>

    -   <span data-ttu-id="f5fc9-128">O serviço do servidor deve ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-128">The server service must be started.</span></span>

    -   <span data-ttu-id="f5fc9-129">A porta 139 do servidor de gerenciamento deve estar aberta para o serviço Web server'sIP.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-129">Port 139 on the Management Server must be open to the Web Service server’sIP.</span></span>

-   <span data-ttu-id="f5fc9-130">Use as listas de controle de acesso (ACLs) para garantir que os pacotes de aplicativos e todos os arquivos de pacote sejam protegidos e não possam ser adulterados.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-130">Use access control lists (ACLs) to ensure that the application packages and all package files are protected and cannot be tampered.</span></span> <span data-ttu-id="f5fc9-131">ACLs restringem o acesso ao local ou à pasta onde você armazena os pacotes, permitindo o acesso somente a determinadas contas.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-131">ACLs restrict access to the location or folder where you store the packages, allowing access only to certain accounts.</span></span>

-   <span data-ttu-id="f5fc9-132">Certifique-se de que o canal entre o servidor de gerenciamento do Application Virtualization e o banco de dados seja protegido — por exemplo, usando IPsec.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-132">Make sure that the channel between the Application Virtualization Management Server and the database is secured—for example, by using IPsec.</span></span>

-   <span data-ttu-id="f5fc9-133">Se os pacotes estiverem armazenados em uma SAN ou NAS, verifique se a conexão entre o dispositivo de armazenamento central e os servidores de virtualização de aplicativo está protegida.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-133">If packages are stored on a SAN or NAS, ensure the connection between the central storage device and the Application Virtualization Servers is protected.</span></span>

-   <span data-ttu-id="f5fc9-134">Todos os canais de comunicação para o cliente devem ser protegidos, incluindo as conexões com o servidor de publicação, o servidor do Application Virtualization e o caminho para os arquivos OSD e ICO, usando um protocolo como HTTPS ou IPsec.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-134">All communication channels to the client should be protected—including connections to the publishing server, the Application Virtualization Server, and the path to the OSD and ICO files—by using a protocol such as HTTPS or IPsec.</span></span> 

-   <span data-ttu-id="f5fc9-135">As permissões de cliente devem ser configuradas para ajudar a garantir que os pacotes não possam ser adulterados por usuários.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-135">Client permissions should be configured to help ensure that packages cannot be tampered with by users.</span></span> <span data-ttu-id="f5fc9-136">É especialmente importante que você não conceda aos usuários permissão para adicionar ou atualizar pacotes em sistemas, como servidores host de sessão de área de trabalho remota (host RDSession) que são compartilhados com vários usuários.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-136">It is especially important that you do not grant users permission to add or update packages on systems, such as Remote Desktop Session Host (RDSession Host) servers, that are shared with multiple users.</span></span>

-   <span data-ttu-id="f5fc9-137">A autenticação Kerberos deve ser permitida em ambientes de floresta ou domínio para que o console de gerenciamento do servidor funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-137">Kerberos authentication must be permitted across domain or forest environments for the Server Management Console to work correctly.</span></span>

-   <span data-ttu-id="f5fc9-138">Esta versão do software não oferece suporte à Hospedagem de um servidor RTSP baseado em Kerberos e a um servidor IIS baseado em Microsoft NTLM somente no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-138">This release of the software does not support hosting a Kerberos-based RTSP server and a Microsoft NTLM-only-based IIS server on the same computer.</span></span> <span data-ttu-id="f5fc9-139">Para hospedar um servidor RTSP e um servidor IIS no mesmo computador, remova o SPN do servidor IIS e use a autenticação NTLM.</span><span class="sxs-lookup"><span data-stu-id="f5fc9-139">To host an RTSP server and an IIS server on the same computer, remove the SPN from the IIS server and use NTLM authentication.</span></span>

## <span data-ttu-id="f5fc9-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5fc9-140">Related topics</span></span>


[<span data-ttu-id="f5fc9-141">Planejamento da implantação do Application Virtualization System</span><span class="sxs-lookup"><span data-stu-id="f5fc9-141">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





