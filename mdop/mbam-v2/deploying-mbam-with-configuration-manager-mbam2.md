---
title: Como implantar o MBAM com o Configuration Manager
description: Como implantar o MBAM com o Configuration Manager
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799275"
---
# Como implantar o MBAM com o Configuration Manager


Os procedimentos a seguir descrevem como implantar o Microsoft BitLocker Administration and Monitoring (MBAM) com o Microsoft System Center Configuration Manager 2007 ou o MicrosoftSystemCenter2012 ConfigurationManager pela configuração recomendada do usingthe, descrito em [introdução-usando MBAM com o Configuration Manager](getting-started---using-mbam-with-configuration-manager.md). A configuração recomendada é instalar os recursos de administração e monitoramento em um ou mais servidores de administração e monitoramento do Microsoft BitLocker e instalar o Microsoft System Center Configuration Manager 2007 ou o MicrosoftSystemCenter2012 ConfigurationManager em um servidor separado.

Antes de iniciar a instalação, verifique se você atendeu os pré-requisitos e requisitos de hardware e software para instalar o MBAM com o Configuration Manager analisando o [planejamento para implantar o MBAM com o Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

Se você precisar reinstalar o MBAM com a topologia do Configuration Manager, será necessário remover determinados objetos do Configuration Manager primeiro. Leia o [artigo da base de dados de conhecimento](https://go.microsoft.com/fwlink/?LinkId=286306) para obter mais informações.

As etapas para instalar o MBAM com o Configuration Manager são agrupadas nas categorias a seguir. Conclua as etapas para cada categoria para concluir a instalação.

## Como criar ou editar os arquivos mof


Para permitir que os computadores cliente relatem detalhes de conformidade do BitLocker através dos relatórios do Gerenciador de configuração do MBAM, você precisa editar o arquivo **Configuration. mof** e editar ou criar o arquivo Sms \ _def. MOF, dependendo de qual versão do Configuration Manager você está usando.

[Como criar ou editar os arquivos mof](how-to-create-or-edit-the-mof-files.md)

## Como instalar o MBAM com o Configuration Manager


Esta seção fornece as etapas sobre como instalar o seguinte: MBAM no servidor do Configuration Manager; os bancos de dados de recuperação e auditoria no servidor de banco de dados; e os recursos do servidor de administração e monitoramento no servidor de administração e monitoramento.

[Como instalar o MBAM com o Configuration Manager](how-to-install-mbam-with-configuration-manager.md)

## Como validar a instalação de recursos do servidor MBAM no servidor do Configuration Manager


Quando a instalação do Microsoft BitLocker Administration and Monitoring for concluída, valide se a instalação configurou com êxito todos os recursos MBAM necessários para o servidor do Configuration Manager.

[Como validar a instalação do MBAM com o Configuration Manager](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## Tópicos relacionados


[Usando o MBAM com o Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





