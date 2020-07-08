---
title: Implantando o Cliente do MBAM 2.0
description: Implantando o Cliente do MBAM 2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799274"
---
# Implantando o Cliente do MBAM 2.0


O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de um sistema de distribuição de software eletrônico, como os serviços de domínio Active Directory, ou diretamente criptografando os computadores cliente como parte do processo de imagem inicial.

Dependendo de quando implantar o cliente de administração e monitoramento do Microsoft BitLocker, você pode habilitar a criptografia do BitLocker em um computador em sua organização antes de o usuário final receber o computador ou depois de configurar a política de grupo e implantar o software cliente do MBAM usando um sistema de implantação de software corporativo.

## Implantar o cliente do MBAM em computadores desktop ou laptop


Depois de configurar a política de grupo, você pode usar um produto do sistema de implantação de software corporativo, como o Microsoft System Center Configuration Manager 2012 ou os serviços de domínio do Active Directory, para implantar os arquivos do Windows Installer da instalação do cliente MBAM em computadores de destino. Você pode implantar o cliente usando os arquivos de 32 bits ou 64 bits MbamClientSetup.exe, ou os arquivos de 32 bits ou 64 bits MBAMClient.msi, que são fornecidos com o software MBAM. Para obter mais informações sobre a implantação de objetos de política de grupo do MBAM, consulte [implantando objetos de política de grupo do MBAM 2,0](deploying-mbam-20-group-policy-objects-mbam-2.md).

[Como implantar o cliente do MBAM em computadores desktop ou notebooks](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## Implantar o cliente MBAM como parte de uma implantação do Windows


Nas organizações em que os computadores são recebidos e configurados centralmente, você pode instalar o cliente MBAM para gerenciar a criptografia do BitLocker em cada computador antes que os dados do usuário sejam gravados nele. A vantagem desse processo é que cada computador está compatível com a criptografia BitLocker. Esse método não depende da ação do usuário porque o administrador já criptografou o computador. Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário. Se a política de grupo foi configurada para exigir um PIN, os usuários são solicitados a definir um PIN depois de receberem a política de grupo.

[Como implantar o cliente do MBAM como parte de uma implantação do Windows](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## Como usar uma linha de comando para instalar o Cliente do MBAM


Esta seção explica como instalar o cliente MBAM usando uma linha de comando.

[Como usar uma linha de comando para instalar o Cliente do MBAM](how-to-use-a-command-line-to-install-the-mbam-client.md)

## Outros recursos para a implantação do cliente MBAM


[Implantando o MBAM 2,0](deploying-mbam-20-mbam-2.md)[planejando a implantação do MBAM 2,0 Client](planning-for-mbam-20-client-deployment-mbam-2.md)

 

 





