---
title: Solução de problemas de permissão de certificado
description: Solução de problemas de permissão de certificado
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796679"
---
# <span data-ttu-id="75df5-103">Solução de problemas de permissão de certificado</span><span class="sxs-lookup"><span data-stu-id="75df5-103">Troubleshooting Certificate Permission Issues</span></span>


<span data-ttu-id="75df5-104">Após a instalação do App-V 4.5, se a chave privada não tiver sido configurada com a ACL apropriada para o serviço de rede, um evento será registrado no log de eventos do NT e uma entrada será colocada no `Sft-server.log` arquivo.</span><span class="sxs-lookup"><span data-stu-id="75df5-104">After the installation of App-V4.5, if the private key has not been configured with the proper ACL for the Network Service, an event is logged in the NT Event Log and an entry is placed in the `Sft-server.log` file.</span></span>

## <span data-ttu-id="75df5-105">Mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="75df5-105">Error Messages</span></span>


### <span data-ttu-id="75df5-106">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="75df5-106">Windows Server2003</span></span>

<span data-ttu-id="75df5-107">ID do evento 36870 — ocorreu um erro fatal ao tentar acessar a chave privada da credencial do servidor SSL.</span><span class="sxs-lookup"><span data-stu-id="75df5-107">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="75df5-108">O código de erro retornado do módulo criptográfico é 0x80090016.</span><span class="sxs-lookup"><span data-stu-id="75df5-108">The error code returned from the cryptographic module is 0x80090016.</span></span>

### <span data-ttu-id="75df5-109">Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="75df5-109">Windows Server2008</span></span>

<span data-ttu-id="75df5-110">ID do evento 36870 — ocorreu um erro fatal ao tentar acessar a chave privada da credencial do servidor SSL.</span><span class="sxs-lookup"><span data-stu-id="75df5-110">Event ID 36870—A fatal error occurred when attempting to access the SSL server credential private key.</span></span> <span data-ttu-id="75df5-111">O código de erro retornado do módulo criptográfico é 0x8009030d.</span><span class="sxs-lookup"><span data-stu-id="75df5-111">The error code returned from the cryptographic module is 0x8009030d.</span></span>

## <span data-ttu-id="75df5-112">SFT-Server. log</span><span class="sxs-lookup"><span data-stu-id="75df5-112">Sft-server.log</span></span>


<span data-ttu-id="75df5-113">O erro a seguir é colocado no `sft-server.log` arquivo localizado no `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` diretório:</span><span class="sxs-lookup"><span data-stu-id="75df5-113">The following error is placed in the `sft-server.log` file located in the `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` directory:</span></span>

<span data-ttu-id="75df5-114">Não foi possível carregar o certificado.</span><span class="sxs-lookup"><span data-stu-id="75df5-114">Certificate could not be loaded.</span></span> <span data-ttu-id="75df5-115">Código de erro \ [-2146893043 \].</span><span class="sxs-lookup"><span data-stu-id="75df5-115">Error code \[-2146893043\].</span></span> <span data-ttu-id="75df5-116">Verifique se a conta de serviço de rede tem acesso adequado ao certificado e seu arquivo de chave particular correspondente.</span><span class="sxs-lookup"><span data-stu-id="75df5-116">Make sure that the Network Service account has proper access to the certificate and its corresponding private key file.</span></span>

 

 





