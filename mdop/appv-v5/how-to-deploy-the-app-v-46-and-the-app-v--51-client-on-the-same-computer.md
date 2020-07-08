---
title: Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador
description: Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796433"
---
# Como implantar o App-V 4,6 e o cliente do App-V 5,1 no mesmo computador

**Observação:** O App-V 4,6 tem saído do suporte básico.

Use as seguintes informações para instalar o cliente do Microsoft Application Virtualization (App-V) 5,1 (preferencialmente, com os service packs e hotfixes mais recentes) e o cliente App-V 4.6 SP2 ou o App-V 4.6 S3 Client no mesmo computador. Para obter as versões, os requisitos e outras informações de planejamento compatíveis, consulte [planejando a migração de uma versão anterior do App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).

**Para implantar o cliente do App-V 5,1 e o aplicativo do App-V 4,6 no mesmo computador**

1.  Instale a versão a seguir do cliente App-V no computador que está executando o App-V 4,6.

    -   [Microsoft Application Virtualization 4,6 Service Pack 3](https://www.microsoft.com/download/details.aspx?id=41187)

2.  Instale o cliente App-V 5,1 no computador que está executando a versão App-V 4,6 SP3 do cliente. Para obter melhores resultados, recomendamos que você instale todas as atualizações disponíveis para o cliente do App-V 5,1.

3.  Converter ou resequenciar os pacotes gradualmente.

    -   Para converter os pacotes, use o conversor de pacotes do App-V 5,1 e converta os pacotes necessários para o formato de arquivo do App-V 5,1 (**. AppV**).

    -   Para resequenciar os pacotes, considere usar a versão mais recente do sequenciador para obter os melhores resultados.

    Para obter mais informações sobre como publicar pacotes, consulte [como publicar um pacote usando o console de gerenciamento](how-to-publish-a-package-by-using-the-management-console-51.md).

4.  Implantar pacotes nos computadores cliente.

5.  Converta os pontos de extensão, conforme necessário. Para obter mais informações, consulte os seguintes recursos:

    -   [Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.1 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [Como converter um pacote criado em uma versão anterior do App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  Teste se seus pacotes do App-V 5,1 foram bem-sucedidos e, em seguida, remova os pacotes do 4,6. Para verificar o estado do usuário dos seus computadores cliente, recomendamos que você use a [virtualização da experiência do usuário](https://technet.microsoft.com/library/dn458947.aspx) ou outra ferramenta de gerenciamento do ambiente do usuário.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Planejamento para a migração de uma versão anterior do App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[Implantação do sequenciador e do cliente App-V 5.1](deploying-the-app-v-51-sequencer-and-client.md)

 

 





