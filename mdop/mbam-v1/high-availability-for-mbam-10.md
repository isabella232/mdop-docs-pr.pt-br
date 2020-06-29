---
title: Alta disponibilidade para o MBAM 1.0
description: Alta disponibilidade para o MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799657"
---
# <span data-ttu-id="403bf-103">Alta disponibilidade para o MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="403bf-103">High Availability for MBAM 1.0</span></span>


<span data-ttu-id="403bf-104">Este tópico descreve como configurar uma instalação altamente disponível do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="403bf-104">This topic describes how to configure a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

## <span data-ttu-id="403bf-105">Cenários de alta disponibilidade para MBAM</span><span class="sxs-lookup"><span data-stu-id="403bf-105">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="403bf-106">O Microsoft BitLocker Administration and Monitoring (MBAM) foi projetado para ser tolerante a falhas.</span><span class="sxs-lookup"><span data-stu-id="403bf-106">Microsoft BitLocker Administration and Monitoring (MBAM) is designed to be fault-tolerant.</span></span> <span data-ttu-id="403bf-107">Se um servidor ficar indisponível, os usuários não devem ser afetados negativamente.</span><span class="sxs-lookup"><span data-stu-id="403bf-107">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="403bf-108">Por exemplo, se o agente do MBAM não puder se conectar ao servidor Web do MBAM, os usuários não devem ser solicitados a confirmar a ação.</span><span class="sxs-lookup"><span data-stu-id="403bf-108">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="403bf-109">Ao planejar a instalação do MBAM, considere as seguintes preocupações que podem afetar a disponibilidade do serviço MBAM:</span><span class="sxs-lookup"><span data-stu-id="403bf-109">When you plan your MBAM installation, consider the following concerns that can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="403bf-110">Criptografia de unidade e senha de recuperação – se uma senha de recuperação não puder ser subprecisada, a criptografia não será iniciada no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="403bf-110">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption will not start on the client computer.</span></span>

-   <span data-ttu-id="403bf-111">Upload de dados de status de conformidade – se o servidor que hospeda o serviço de relatório de status de conformidade não estiver disponível, os dados de conformidade não permanecerão atuais.</span><span class="sxs-lookup"><span data-stu-id="403bf-111">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data will not remain current.</span></span>

-   <span data-ttu-id="403bf-112">Acesso à chave de recuperação do suporte técnico-se o suporte técnico não conseguir acessar as informações do banco de dados do MBAM, não será possível fornecer chaves de recuperação para os usuários.</span><span class="sxs-lookup"><span data-stu-id="403bf-112">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, they will be unable to provide recovery keys to users.</span></span>

-   <span data-ttu-id="403bf-113">Disponibilidade de relatórios – os relatórios não estarão disponíveis se o servidor que hospeda os relatórios de conformidade e auditoria não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="403bf-113">Availability of reports – Reports will not be available if the server that hosts the Compliance and Audit Reports is not available.</span></span>

<span data-ttu-id="403bf-114">A principal preocupação para o MBAM High Availability é a disponibilidade da chave de recuperação do BitLocker.</span><span class="sxs-lookup"><span data-stu-id="403bf-114">The main concern for MBAM high availability is BitLocker key recovery availability.</span></span> <span data-ttu-id="403bf-115">Se o suporte técnico não puder fornecer chaves de recuperação, os usuários bloqueados não poderão desbloquear seus computadores.</span><span class="sxs-lookup"><span data-stu-id="403bf-115">If the help desk cannot provide recovery keys, users who are locked out cannot unlock their computers.</span></span> <span data-ttu-id="403bf-116">Para evitar esse problema, considere a implementação de servidores da Web redundantes e bancos de dados para garantir alta disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="403bf-116">To avoid this problem, consider implementing redundant web servers and databases to ensure high availability.</span></span>

<span data-ttu-id="403bf-117">Para obter mais informações sobre a escalabilidade de MBAM e alta disponibilidade, consulte o [White Paper de redimensionamento de MBAM](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .</span><span class="sxs-lookup"><span data-stu-id="403bf-117">For more information about MBAM scalability and high availability, see the [MBAM Scalability White Paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) (https://go.microsoft.com/fwlink/p/?LinkId=229025).</span></span>

<span data-ttu-id="403bf-118">Para obter orientação geral sobre a alta disponibilidade do Microsoft SQL Server, consulte [alta disponibilidade](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .</span><span class="sxs-lookup"><span data-stu-id="403bf-118">For general guidance on high availability for Microsoft SQL Server, see [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) (https://go.microsoft.com/fwlink/p/?LinkId=221504).</span></span>

<span data-ttu-id="403bf-119">Para obter orientação geral sobre a disponibilidade e a escalabilidade para servidores Web, consulte [disponibilidade e escalabilidade](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .</span><span class="sxs-lookup"><span data-stu-id="403bf-119">For general guidance on availability and scalability for web servers, see [Availability and Scalability](https://go.microsoft.com/fwlink/p/?LinkId=221503) (https://go.microsoft.com/fwlink/p/?LinkId=221503).</span></span>

## <span data-ttu-id="403bf-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="403bf-120">Related topics</span></span>


[<span data-ttu-id="403bf-121">Manutenção do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="403bf-121">Maintaining MBAM 1.0</span></span>](maintaining-mbam-10.md)

 

 





