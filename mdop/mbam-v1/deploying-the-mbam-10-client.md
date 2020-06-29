---
title: Implantando o Cliente do MBAM 1.0
description: Implantando o Cliente do MBAM 1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799165"
---
# Implantando o Cliente do MBAM 1.0


O cliente Microsoft BitLocker Administration and Monitoring (MBAM) permite que os administradores imponham e monitorem a criptografia de unidade de disco BitLocker em computadores da empresa. O cliente BitLocker pode ser integrado a uma organização implantando o cliente por meio de ferramentas como os serviços de domínio do Active Directory ou diretamente criptografando os computadores cliente como parte do processo de imagem inicial.

Dependendo de quando implantar o cliente do MBAM, você pode habilitar a criptografia do BitLocker em um computador em sua organização antes ou depois que o usuário final receber o computador. Para controlar esse tempo, configure a política de grupo e implante o software cliente do MBAM usando um sistema de implantação de software corporativo.

Você pode usar um ou ambos os métodos em sua organização. Se você usa os dois métodos, pode melhorar a conformidade, o relatório e o suporte à recuperação de chave.

## Implantar o cliente do MBAM em computadores desktop ou laptop


Depois de configurar a política de grupo, você pode implantar os arquivos do Windows Installer de instalação do cliente do MBAM em computadores de destino. Você pode fazer isso usando um produto de sistema de implantação de software corporativo, como o Gerenciador de configuração do Microsoft System Center 2012 ou os serviços de domínio do Active Directory. Os dois arquivos disponíveis do Windows Installer da instalação do cliente MBAM são MBAMClient-64bit.msi e MBAMClient-32bit.msi. Esses arquivos são fornecidos com o software MBAM. Para obter mais informações sobre como implantar objetos de política de grupo do MBAM, consulte [implantando objetos de política de grupo do MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

[Como implantar o cliente do MBAM em computadores desktop ou notebooks](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## Implantar o cliente MBAM como parte de uma implantação do Windows


Em algumas organizações, novos computadores são recebidos e configurados centralmente. Essa situação permite que os administradores instalem o cliente do MBAM para gerenciar a criptografia do BitLocker em cada computador antes que todos os dados do usuário sejam gravados no computador. Essa abordagem ajuda a garantir que os computadores sejam criptografados corretamente porque o administrador executa a ação sem depender de uma ação do usuário final. Uma pressuposição chave para esse cenário é que a política da organização instala uma imagem corporativa do Windows antes que o computador seja entregue ao usuário.

[Como implantar o cliente do MBAM como parte de uma implantação do Windows](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## Outros recursos para a implantação do cliente MBAM


[Implantando o MBAM 1.0](deploying-mbam-10.md)

[Planejar implantação de cliente MBAM 1.0](planning-for-mbam-10-client-deployment.md)

 

 





