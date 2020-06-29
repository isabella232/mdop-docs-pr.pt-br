---
title: Alta disponibilidade para o MBAM 2.0
description: Alta disponibilidade para o MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799530"
---
# <span data-ttu-id="65fb8-103">Alta disponibilidade para o MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="65fb8-103">High Availability for MBAM 2.0</span></span>


<span data-ttu-id="65fb8-104">Este tópico fornece informações básicas sobre uma instalação altamente disponível do Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="65fb8-104">This topic provides basic information about a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="65fb8-105">Não há suporte total para cenários de alta disponibilidade nesta versão do MBAM para que eles não sejam descritos aqui.</span><span class="sxs-lookup"><span data-stu-id="65fb8-105">High-availability scenarios are not fully supported in this version of MBAM, so they are not described here.</span></span> <span data-ttu-id="65fb8-106">É recomendável Pesquisar Blogs e fóruns relacionados, onde os usuários descrevem como eles configuraram com êxito a alta disponibilidade para o MBAM em seus ambientes.</span><span class="sxs-lookup"><span data-stu-id="65fb8-106">It is recommended that you search related blogs and forums, where users describe how they have successfully configured high availability for MBAM in their environments.</span></span>

## <span data-ttu-id="65fb8-107">Cenários de alta disponibilidade para MBAM</span><span class="sxs-lookup"><span data-stu-id="65fb8-107">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="65fb8-108">A administração e o monitoramento do Microsoft BitLocker são projetados para serem tolerantes a falhas.</span><span class="sxs-lookup"><span data-stu-id="65fb8-108">Microsoft BitLocker Administration and Monitoring is designed to be fault-tolerant.</span></span> <span data-ttu-id="65fb8-109">Se um servidor ficar indisponível, os usuários não devem ser afetados negativamente.</span><span class="sxs-lookup"><span data-stu-id="65fb8-109">If a server becomes unavailable, users should not be negatively affected.</span></span> <span data-ttu-id="65fb8-110">Por exemplo, se o agente do MBAM não puder se conectar ao servidor Web do MBAM, os usuários não devem ser solicitados a confirmar a ação.</span><span class="sxs-lookup"><span data-stu-id="65fb8-110">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="65fb8-111">Ao planejar a instalação do MBAM, considere os seguintes itens, que podem afetar a disponibilidade do serviço MBAM:</span><span class="sxs-lookup"><span data-stu-id="65fb8-111">When you plan your MBAM installation, consider the following items, which can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="65fb8-112">Criptografia de unidade e senha de recuperação – se não for possível a caução de uma senha de recuperação, a criptografia não será iniciada no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="65fb8-112">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption does not start on the client computer.</span></span>

-   <span data-ttu-id="65fb8-113">Upload de dados de status de conformidade – se o servidor que hospeda o serviço de relatório de status de conformidade não estiver disponível, os dados de conformidade não permanecerão atualizados.</span><span class="sxs-lookup"><span data-stu-id="65fb8-113">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data does not remain current.</span></span>

-   <span data-ttu-id="65fb8-114">Acesso à chave de recuperação do suporte técnico-se o suporte técnico não conseguir acessar as informações do banco de dados do MBAM, o suporte técnico não poderá fornecer chaves de recuperação para os usuários.</span><span class="sxs-lookup"><span data-stu-id="65fb8-114">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, the Help Desk cannot provide recovery keys to users.</span></span>

-   <span data-ttu-id="65fb8-115">Disponibilidade de relatórios – se o servidor que hospeda os relatórios de conformidade e auditoria não estiver disponível, os relatórios não estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="65fb8-115">Availability of reports –If the server that hosts the Compliance and Audit Reports is not available, reports will not be available.</span></span>

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a><span data-ttu-id="65fb8-116">Como o MBAM backup usa o VSS (Volume Shadow Copy Service)</span><span class="sxs-lookup"><span data-stu-id="65fb8-116">How the MBAM Backup Uses the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="65fb8-117">O MBAM 2.0 oferece um gravador VSS (Volume Shadow Copy Service), chamado de Microsoft BitLocker Administration and Management Writer, que facilita o backup do banco de dados de conformidade e auditoria e do banco de dados de recuperação.</span><span class="sxs-lookup"><span data-stu-id="65fb8-117">MBAM2.0 provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer, which facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="65fb8-118">O instalador do Windows Server do MBAM registra o gravador VSS do MBAM.</span><span class="sxs-lookup"><span data-stu-id="65fb8-118">The MBAM Server Windows Installer registers the MBAM VSS Writer.</span></span> <span data-ttu-id="65fb8-119">Qualquer falha durante o registro do gravador VSS faz com que a instalação do servidor do MBAM seja revertida.</span><span class="sxs-lookup"><span data-stu-id="65fb8-119">Any failure during the VSS writer registration causes the MBAM Server installation to roll back.</span></span> <span data-ttu-id="65fb8-120">Em uma topologia em que o banco de dados de conformidade e auditoria e o banco de dados de recuperação são instalados em servidores diferentes, uma instância separada do gravador VSS do MBAM está registrada em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="65fb8-120">In a topology where the Compliance and Audit Database and the Recovery Database are installed on different servers, a separate instance of MBAM VSS Writer is registered on each server.</span></span> <span data-ttu-id="65fb8-121">O gravador VSS do MBAM depende do gravador VSS do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="65fb8-121">The MBAM VSS Writer is dependent on the SQL Server VSS Writer.</span></span> <span data-ttu-id="65fb8-122">O gravador VSS do SQL Server está registrado como parte da instalação do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="65fb8-122">The SQL Server VSS Writer is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="65fb8-123">Qualquer tecnologia de backup que usa gravadores VSS para executar o backup pode descobrir o gravador VSS do MBAM.</span><span class="sxs-lookup"><span data-stu-id="65fb8-123">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS Writer.</span></span>

## <span data-ttu-id="65fb8-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65fb8-124">Related topics</span></span>


[<span data-ttu-id="65fb8-125">Manutenção do MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="65fb8-125">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)

 

 





