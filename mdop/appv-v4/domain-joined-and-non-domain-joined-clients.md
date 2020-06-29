---
title: Clientes ingressados no domínio e não ingressados no domínio
description: Clientes ingressados no domínio e não ingressados no domínio
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797964"
---
# <span data-ttu-id="287b4-103">Clientes ingressados no domínio e não ingressados no domínio</span><span class="sxs-lookup"><span data-stu-id="287b4-103">Domain-Joined and Non-Domain-Joined Clients</span></span>


<span data-ttu-id="287b4-104">O cliente da área de trabalho App-V pode ser configurado para permitir a conexão a uma rede independentemente de o cliente ter ingressado no domínio ou não no domínio.</span><span class="sxs-lookup"><span data-stu-id="287b4-104">The App-V Desktop Client can be configured to allow connection to a network regardless of whether the client is domain joined or non-domain joined.</span></span>

## <span data-ttu-id="287b4-105">Clientes associados a um domínio</span><span class="sxs-lookup"><span data-stu-id="287b4-105">Domain-Joined Clients</span></span>


<span data-ttu-id="287b4-106">Os clientes que fazem parte do domínio, mas fora da rede interna, podem se comunicar com a infraestrutura do App-V usando uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="287b4-106">Clients that are domain joined, but outside the internal network, can communicate with the App-V infrastructure by using a VPN connection.</span></span> <span data-ttu-id="287b4-107">Quando quiser fornecer aos usuários a capacidade de sair da rede interna, mas continuar a se comunicar em uma infraestrutura do App-V, seu ambiente requer muito pouca configuração.</span><span class="sxs-lookup"><span data-stu-id="287b4-107">When you want to provide users the ability to leave the internal network but still communicate in an App-V infrastructure, your environment requires very little setup.</span></span> <span data-ttu-id="287b4-108">Como os usuários já fazem parte do domínio, você só precisa garantir que as credenciais armazenadas em cache sejam compatíveis com o cliente.</span><span class="sxs-lookup"><span data-stu-id="287b4-108">Because the users are already part of the domain, you simply need to ensure that Cached Credentials are supported on the client.</span></span> <span data-ttu-id="287b4-109">Essa é a configuração padrão, e todas as alterações feitas a essa configuração podem ser realizadas em políticas de grupo.</span><span class="sxs-lookup"><span data-stu-id="287b4-109">This is the default configuration, and any changes to this setting can be accomplished from Group Policies.</span></span>

<span data-ttu-id="287b4-110">Conforme mencionado no guia de práticas recomendadas de segurança do App-V, o usuário tentará enviar sua permissão de usuário para a infraestrutura do App-V para autenticação.</span><span class="sxs-lookup"><span data-stu-id="287b4-110">As mentioned in the App-V Security Best Practices Guide, the user will attempt to send their user ticket to the App-V infrastructure for authentication.</span></span> <span data-ttu-id="287b4-111">Se a permissão estiver vencida, ela será revertida para usar NTLM e as credenciais armazenadas em cache no computador.</span><span class="sxs-lookup"><span data-stu-id="287b4-111">If the ticket is expired, it will revert to using NTLM and the cached credentials on the computer.</span></span> <span data-ttu-id="287b4-112">Para permitir o roaming, os administradores devem garantir que o servidor de publicação que está sendo acessado internamente está disponível no mesmo nome externamente para que os nomes sejam resolvidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="287b4-112">To allow roaming, administrators must ensure that the publishing server being accessed internally is available at the same name externally for the names to resolve properly.</span></span>

## <span data-ttu-id="287b4-113">Clientes que não fazem parte do domínio</span><span class="sxs-lookup"><span data-stu-id="287b4-113">Non-Domain-Joined Clients</span></span>


<span data-ttu-id="287b4-114">Os clientes que não ingressaram no domínio, mas precisam se comunicar na infraestrutura do App-V devem ser configurados para garantir que a autenticação para a infraestrutura do App-V seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="287b4-114">Clients that are non-domain joined but need to communicate in the App-V infrastructure must be configured to ensure that authentication to the App-V infrastructure is successful.</span></span> <span data-ttu-id="287b4-115">O cliente da área de trabalho do App-V não permite solicitação para o processo de atualização de publicação, portanto, o cliente deve ser configurado para apresentar as credenciais adequadas para o servidor de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="287b4-115">The App-V Desktop Client does not permit prompting for the publishing refresh process, so the client must be configured to present the proper credentials to the App-V Management Server.</span></span>

<span data-ttu-id="287b4-116">O servidor de publicação, que é configurado para publicação de atualização do cliente que não ingressou no domínio, requer que o nome externo que o acesso aos clientes esteja configurado como o nome comum ou um nome alternativo de assunto (SAN) no certificado do servidor de publicação.</span><span class="sxs-lookup"><span data-stu-id="287b4-116">The publishing server, which is configured for publishing refresh from the non-domain joined client, requires that the external name that clients access is configured as the common name or a subject alternate name (SAN) on the publishing server’s certificate.</span></span>

## <span data-ttu-id="287b4-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="287b4-117">Related topics</span></span>


[<span data-ttu-id="287b4-118">Como atribuir as credenciais adequadas para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="287b4-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

[<span data-ttu-id="287b4-119">Como atribuir as credenciais adequadas para o Windows XP</span><span class="sxs-lookup"><span data-stu-id="287b4-119">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





