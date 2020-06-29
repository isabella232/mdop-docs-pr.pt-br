---
title: Problemas Conhecidos na Versão Internacional do MBAM
description: Problemas Conhecidos na Versão Internacional do MBAM
author: dansimp
ms.assetid: bbf888dc-93c1-4323-b43c-0ded098e9b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af32551135ff297d25930f94b40bf04c0fcaaafe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799742"
---
# <span data-ttu-id="c6e18-103">Problemas Conhecidos na Versão Internacional do MBAM</span><span class="sxs-lookup"><span data-stu-id="c6e18-103">Known Issues in the MBAM International Release</span></span>

<span data-ttu-id="c6e18-104">Esta seção contém problemas conhecidos do lançamento do Microsoft BitLocker Administration and Monitoring (MBAM) International.</span><span class="sxs-lookup"><span data-stu-id="c6e18-104">This section contains known issues for Microsoft BitLocker Administration and Monitoring (MBAM) International Release.</span></span>

## <span data-ttu-id="c6e18-105">Problemas Conhecidos na Versão Internacional do MBAM</span><span class="sxs-lookup"><span data-stu-id="c6e18-105">Known Issues in the MBAM International Release</span></span>

### <span data-ttu-id="c6e18-106">O processo de instalação não especifica a atualização</span><span class="sxs-lookup"><span data-stu-id="c6e18-106">The Installation Process Does Not Specify Update</span></span>

<span data-ttu-id="c6e18-107">Após a atualização do servidor ou servidores de administração e monitoramento do Microsoft BitLocker, o programa de instalação não afirma que uma atualização está sendo instalada.</span><span class="sxs-lookup"><span data-stu-id="c6e18-107">Upon updating the Microsoft BitLocker Administration and Monitoring server or servers, the Setup program does not state that an update is being installed.</span></span>

<span data-ttu-id="c6e18-108">**Solução alternativa**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="c6e18-108">**Workaround**: None.</span></span>

### <span data-ttu-id="c6e18-109">Certificados usados para a função de servidor de administração e monitoramento</span><span class="sxs-lookup"><span data-stu-id="c6e18-109">Certificates Used for the Administration and Monitoring Server Role</span></span>

<span data-ttu-id="c6e18-110">Se você estiver usando um certificado para autenticação entre servidores do MBAM, após a atualização do servidor de administração e monitoramento do MBAM, você deve garantir que o certificado seja válido e não revogado ou expirado.</span><span class="sxs-lookup"><span data-stu-id="c6e18-110">If you are using a certificate for authentication between MBAM servers, after updating the MBAM Administration and Monitoring server you must ensure that the certificate is valid and not revoked or expired.</span></span>

<span data-ttu-id="c6e18-111">**Solução alternativa**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="c6e18-111">**Workaround**: None.</span></span>

### <span data-ttu-id="c6e18-112">MBAM svclog preenchendo espaço em disco</span><span class="sxs-lookup"><span data-stu-id="c6e18-112">MBAM Svclog File Filling Disk Space</span></span>

<span data-ttu-id="c6e18-113">Se você seguiu o [artigo da base de dados de conhecimento 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), talvez seja necessário repetir as etapas do KB após a instalação desta atualização.</span><span class="sxs-lookup"><span data-stu-id="c6e18-113">If you have followed [Knowledge Base article 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), you might have to repeat the KB steps after you install this update.</span></span>

<span data-ttu-id="c6e18-114">**Solução alternativa**: nenhum.</span><span class="sxs-lookup"><span data-stu-id="c6e18-114">**Workaround**: None.</span></span>

## <span data-ttu-id="c6e18-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6e18-115">Related topics</span></span>

[<span data-ttu-id="c6e18-116">Implantação da Atualização da Versão de Idioma do MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="c6e18-116">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





