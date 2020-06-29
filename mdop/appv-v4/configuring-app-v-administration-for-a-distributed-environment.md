---
title: Configuração da administração do App-V para um ambiente distribuído
description: Configuração da administração do App-V para um ambiente distribuído
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10798020"
---
# <span data-ttu-id="7af5f-103">Configuração da administração do App-V para um ambiente distribuído</span><span class="sxs-lookup"><span data-stu-id="7af5f-103">Configuring App-V Administration for a Distributed Environment</span></span>


<span data-ttu-id="7af5f-104">Ao projetar a infraestrutura de sua organização específica, você pode instalar o serviço Web de gerenciamento do App-V em um computador diferente do computador em que você instala o servidor de gerenciamento do App-V.</span><span class="sxs-lookup"><span data-stu-id="7af5f-104">When designing the infrastructure for your specific organization, you can install the App-V Management Web Service on a computer other than the computer where you install the App-V Management Server.</span></span> <span data-ttu-id="7af5f-105">Os motivos comuns para separar esses componentes do App-V incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7af5f-105">Common reasons for separating these App-V components include the following:</span></span>

-   <span data-ttu-id="7af5f-106">Desempenho</span><span class="sxs-lookup"><span data-stu-id="7af5f-106">Performance</span></span>

-   <span data-ttu-id="7af5f-107">Confiabilidade</span><span class="sxs-lookup"><span data-stu-id="7af5f-107">Reliability</span></span>

-   <span data-ttu-id="7af5f-108">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="7af5f-108">Availability</span></span>

-   <span data-ttu-id="7af5f-109">Escalabilidade</span><span class="sxs-lookup"><span data-stu-id="7af5f-109">Scalability</span></span>

<span data-ttu-id="7af5f-110">Separar o servidor de gerenciamento e o serviço Web de gerenciamento exige configuração adicional para que a infraestrutura opere corretamente.</span><span class="sxs-lookup"><span data-stu-id="7af5f-110">Separating the Management Server and Management Web Service requires additional configuration for the infrastructure to operate correctly.</span></span> <span data-ttu-id="7af5f-111">Quando você separa esses dois recursos, mas não conclua os procedimentos descritos neste tópico, o console de gerenciamento se conectará ao serviço Web de gerenciamento, mas não poderá ser autenticado corretamente com o repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="7af5f-111">When you separate these two features but do not complete the procedures described in this topic, the Management Console will connect to the Management Web Service but will not be able to properly authenticate with the data store.</span></span> <span data-ttu-id="7af5f-112">O console de gerenciamento não será carregado corretamente, e o administrador não será capaz de concluir tarefas administrativas.</span><span class="sxs-lookup"><span data-stu-id="7af5f-112">The Management Console will not load properly, and the administrator will not be able to complete any administrative tasks.</span></span>

<span data-ttu-id="7af5f-113">Esse comportamento ocorre porque o serviço Web de gerenciamento não pode usar as credenciais, transmitidas a ele pelo console de gerenciamento, para acessar o repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="7af5f-113">This behavior occurs because the Management Web Service cannot use the credentials, passed to it from the Management Console, to access the data store.</span></span> <span data-ttu-id="7af5f-114">A solução é configurar o servidor de serviços Web de gerenciamento como "confiável para delegação".</span><span class="sxs-lookup"><span data-stu-id="7af5f-114">The solution is to configure the Management Web Service server to be “Trusted for delegation.”</span></span>

## <span data-ttu-id="7af5f-115">Configurar os serviços de domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="7af5f-115">Configuring Active Directory Domain Services</span></span>


<span data-ttu-id="7af5f-116">Também é necessário configurar adequadamente os serviços de domínio do Active Directory para que funcionem em um ambiente distribuído.</span><span class="sxs-lookup"><span data-stu-id="7af5f-116">It is also necessary to configure Active Directory Domain Services properly to work in a distributed environment.</span></span> <span data-ttu-id="7af5f-117">Esta seção inclui as informações de que você precisa para configurar os serviços de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7af5f-117">This section includes the information you need configure Active Directory Domain Services.</span></span>

### <span data-ttu-id="7af5f-118">Quando o SQL Service usa a conta do sistema local</span><span class="sxs-lookup"><span data-stu-id="7af5f-118">When SQL Service Uses Local System account</span></span>

<span data-ttu-id="7af5f-119">Para configurar o ambiente em que o serviço SQL usa a conta do sistema local, altere as propriedades da conta do computador do serviço Web de gerenciamento para serem confiáveis para delegação.</span><span class="sxs-lookup"><span data-stu-id="7af5f-119">To set up the environment where the SQL Service uses the local system account, change the properties of the machine account of the Management Web Service to be trusted for delegation.</span></span> <span data-ttu-id="7af5f-120">Para obter procedimentos detalhados sobre como fazer isso, consulte [como configurar o servidor para ser confiável para delegação](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span><span class="sxs-lookup"><span data-stu-id="7af5f-120">For detailed procedures about how to do this, see [How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span></span>

### <span data-ttu-id="7af5f-121">Quando o serviço SQL usa uma conta baseada em domínio</span><span class="sxs-lookup"><span data-stu-id="7af5f-121">When SQL Service Uses Domain-Based Account</span></span>

<span data-ttu-id="7af5f-122">Para configurar o ambiente em que os servidores SQL usam contas de serviço baseadas em domínio, você precisa considerar se uma série de fatores se aplica, incluindo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7af5f-122">To set up the environment where SQL Servers use domain-based service accounts, you need to consider whether or not a variety of factors apply, including the following:</span></span>

-   <span data-ttu-id="7af5f-123">Clustering do SQL Server</span><span class="sxs-lookup"><span data-stu-id="7af5f-123">Clustering of SQL Server</span></span>

-   <span data-ttu-id="7af5f-124">Replicação</span><span class="sxs-lookup"><span data-stu-id="7af5f-124">Replication</span></span>

-   <span data-ttu-id="7af5f-125">Tarefas automatizadas</span><span class="sxs-lookup"><span data-stu-id="7af5f-125">Automated tasks</span></span>

-   <span data-ttu-id="7af5f-126">Servidores vinculados</span><span class="sxs-lookup"><span data-stu-id="7af5f-126">Linked servers</span></span>

<span data-ttu-id="7af5f-127">Para obter informações sobre como configurar os serviços de domínio Active Directory quando o serviço SQL usa uma conta baseada em domínio, consulte <https://go.microsoft.com/fwlink/?LinkId=151968> .</span><span class="sxs-lookup"><span data-stu-id="7af5f-127">For information about configuring Active Directory Domain Services when the SQL service uses a domain-based account, see <https://go.microsoft.com/fwlink/?LinkId=151968>.</span></span>

 

 





