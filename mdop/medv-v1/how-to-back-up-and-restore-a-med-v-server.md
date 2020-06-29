---
title: Como fazer backup e restaurar um servidor do MED-V
description: Como fazer backup e restaurar um servidor do MED-V
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799202"
---
# Como fazer backup e restaurar um servidor do MED-V


É possível fazer o backup dos arquivos XML localizados no servidor e depois restaurá-los em caso de perda de dados no servidor.

**Para fazer backup de um servidor MED-V**

-   Faça backup dos seguintes arquivos, localizados em * &lt; installdir &gt; \\Servers\\ConfigurationServer*:

    **Observação**  Se a configuração tiver sido alterada do padrão, os arquivos poderão estar armazenados em um local diferente.

     

    -   ClientPolicy.xml

    -   ClientSettings.xml

    -   ConfigurationFiles.xml

    -   OrganizationPolicy.xml

    -   WorkspaceKeys.xml

    **Observação**  Também é possível fazer o backup do arquivo ServerSettings.xml. No entanto, se uma configuração específica tiver sido alterada (por exemplo, no servidor original, o diretório de VMS do MED-V está localizado em "*C:\\Vms*" e tal diretório não existe no novo servidor), ele pode causar um erro.

     

**Para restaurar um servidor MED-V**

1.  Instale um novo servidor MED-V.

2.  Copie os arquivos de backup para o seguinte diretório:

    *&lt;InstallDir &gt; \\Servers\\ConfigurationServer*

3.  Reinicie o serviço MED-V.

 

 





