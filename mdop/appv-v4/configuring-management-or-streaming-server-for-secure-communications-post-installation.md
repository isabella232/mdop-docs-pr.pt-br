---
title: Configuração do servidor de gerenciamento ou de streaming para comunicações seguras após a instalação
description: Configuração do servidor de gerenciamento ou de streaming para comunicações seguras após a instalação
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798013"
---
# <span data-ttu-id="6ebfa-103">Configuração do servidor de gerenciamento ou de streaming para comunicações seguras após a instalação</span><span class="sxs-lookup"><span data-stu-id="6ebfa-103">Configuring Management or Streaming Server for Secure Communications Post-Installation</span></span>


<span data-ttu-id="6ebfa-104">Se o certificado correto não era provisionado antes da instalação do servidor de gerenciamento do App-V ou do App-V Streaming Server, o App-V pode ser configurado para melhorar a segurança após a instalação inicial.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-104">If the proper certificate was not provisioned before the installation of the App-V Management Server or the App-V Streaming Server, App-V can be configured for enhanced security after the initial installation.</span></span> <span data-ttu-id="6ebfa-105">Você pode configurar o servidor de gerenciamento do App-V por meio do console de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-105">You can configure the App-V Management Server through the App-V Management Console.</span></span> <span data-ttu-id="6ebfa-106">No entanto, o servidor de streaming App-V é gerenciado por meio do registro.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-106">However, the App-V Streaming Server is managed through the registry.</span></span> <span data-ttu-id="6ebfa-107">Em ambos os casos, o certificado deve incluir o *uso de chave estendida* (EKU) adequado para autenticação do servidor e o serviço de rede deve ter acesso de leitura à chave privada.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-107">In either case, the certificate must include the proper *extended key usage* (EKU) for Server authentication and the Network Service must have read access to the private key.</span></span>

## <span data-ttu-id="6ebfa-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6ebfa-108">In This Section</span></span>


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[<span data-ttu-id="6ebfa-109">Como configurar a segurança do servidor de gerenciamento após a instalação</span><span class="sxs-lookup"><span data-stu-id="6ebfa-109">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)  
<span data-ttu-id="6ebfa-110">Fornece um procedimento que pode ser executado após a instalação, usando o console de gerenciamento do App-V, para adicionar o certificado e configurar o servidor de gerenciamento do App-V para segurança aprimorada.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-110">Provides a procedure that can be performed post-installation, using the App-V Management Console, to add the certificate and configure the App-V Management Server for enhanced security.</span></span>

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[<span data-ttu-id="6ebfa-111">Como configurar a segurança do servidor de streaming após a instalação</span><span class="sxs-lookup"><span data-stu-id="6ebfa-111">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)  
<span data-ttu-id="6ebfa-112">Fornece um procedimento que pode ser executado após a instalação, para adicionar o certificado e configurar o servidor de streaming App-V para segurança aprimorada.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-112">Provides a procedure that can be performed post-installation, to add the certificate and configure the App-V Streaming Server for enhanced security.</span></span>

<a href="" id="troubleshooting-certificate-permission-issues"></a>[<span data-ttu-id="6ebfa-113">Solução de problemas de permissão de certificado</span><span class="sxs-lookup"><span data-stu-id="6ebfa-113">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)  
<span data-ttu-id="6ebfa-114">Fornece orientação de solução de problemas para quando a chave privada não tiver sido configurada com a ACL apropriada para o serviço de rede.</span><span class="sxs-lookup"><span data-stu-id="6ebfa-114">Provides troubleshooting guidance for when the private key has not been configured with the proper ACL for the Network Service.</span></span>

 

 





