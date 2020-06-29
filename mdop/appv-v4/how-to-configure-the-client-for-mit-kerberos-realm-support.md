---
title: Como configurar o cliente para suporte de realm MIT Kerberos
description: Como configurar o cliente para suporte de realm MIT Kerberos
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797200"
---
# <span data-ttu-id="72292-103">Como configurar o cliente para suporte de realm MIT Kerberos</span><span class="sxs-lookup"><span data-stu-id="72292-103">How to Configure the Client for MIT Kerberos Realm Support</span></span>


<span data-ttu-id="72292-104">No Application Virtualization (App-V) 4,5 SP1, foi adicionado suporte para territórios de MIT Kerberos.</span><span class="sxs-lookup"><span data-stu-id="72292-104">In Application Virtualization (App-V) 4.5 SP1, support was added for MIT Kerberos realms.</span></span> <span data-ttu-id="72292-105">Este tópico fornece informações detalhadas sobre como habilitar esse suporte.</span><span class="sxs-lookup"><span data-stu-id="72292-105">This topic provides detailed information on how to enable that support.</span></span>

**<span data-ttu-id="72292-106">Para habilitar o suporte a territórios Kerberos MIT</span><span class="sxs-lookup"><span data-stu-id="72292-106">To enable support for MIT Kerberos Realms</span></span>**

-   <span data-ttu-id="72292-107">Crie uma nova chave do registro chamada **UseMitKerberos** do tipo DWORD, da seguinte maneira, e defina-a como um valor igual a 1.</span><span class="sxs-lookup"><span data-stu-id="72292-107">Create a new registry key named **UseMitKerberos** of type DWORD, as follows, and then set it to a value of 1.</span></span>

    <span data-ttu-id="72292-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span><span class="sxs-lookup"><span data-stu-id="72292-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span></span>

 

 





