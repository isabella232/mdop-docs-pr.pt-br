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
# Como configurar o cliente para suporte de realm MIT Kerberos


No Application Virtualization (App-V) 4,5 SP1, foi adicionado suporte para territórios de MIT Kerberos. Este tópico fornece informações detalhadas sobre como habilitar esse suporte.

**Para habilitar o suporte a territórios Kerberos MIT**

-   Crie uma nova chave do registro chamada **UseMitKerberos** do tipo DWORD, da seguinte maneira, e defina-a como um valor igual a 1.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos

 

 





