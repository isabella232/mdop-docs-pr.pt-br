---
title: Como criar ou editar os arquivos mof
description: Como criar ou editar os arquivos mof
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799649"
---
# Como criar ou editar os arquivos mof


Antes de instalar o Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, você precisa editar o arquivo Configuration. mof. Você também precisará editar ou criar o arquivo SMS \ _def. MOF, dependendo de qual versão do Configuration Manager você está usando.

## Edite o arquivo Configuration.mof


Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker por meio dos relatórios do Gerenciador de configuração do MBAM, você precisa editar o arquivo Configuration. mof do Microsoft System Center Configuration Manager 2007 e do SystemCenter2012 ConfigurationManager.

[Edite o arquivo Configuration.mof](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Criar ou editar o arquivo SMS \ _def. mof


Para permitir que os computadores cliente relatem os detalhes de conformidade do BitLocker nos relatórios do Gerenciador de configuração do MBAM, você precisa criar ou editar o arquivo SMS \ _def. mof. No Configuration Manager 2007, o arquivo já existe, portanto, você precisa editar, mas não substituir, o arquivo existente. Se estiver usando o SystemCenter2012 ConfigurationManager, você deve criar o arquivo.

[Criar ou editar o arquivo SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md)

## Tópicos relacionados


[Como implantar o MBAM com o Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





