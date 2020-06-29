---
title: Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador
description: Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796435"
---
# Como implantar o App-V 4,6 e o cliente do App-V 5,0 no mesmo computador

**Observação:** O App-V 4,6 tem saído do suporte básico. O seguinte pressupõe que o cliente App-V 4,6 SP3 já está instalado.

Use as informações a seguir para instalar o cliente do App-V 5,0 (de preferência, com os service packs e hotfixes mais recentes) e o aplicativo App-V 4.6 SP3 no mesmo computador. Para obter as versões, os requisitos e outras informações de planejamento compatíveis, consulte [planejando a migração de uma versão anterior do App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).

**Para implantar o cliente do App-V 5,0 e o aplicativo do App-V 4,6 no mesmo computador**

1.  Instale o cliente do App-V 5,0 SP3 no computador que está executando a versão do App-V 4,6 do cliente. Para obter melhores resultados, recomendamos que você instale todas as atualizações disponíveis para o cliente App-V 5,0 SP3.

2.  Converter ou resequenciar os pacotes gradualmente.

    -   Para converter os pacotes, use o conversor de pacotes do App-V 5,0 e converta os pacotes necessários para o formato de arquivo do App-V 5,0 (**. AppV**).

    -   Para resequenciar os pacotes, considere usar a versão mais recente do sequenciador para obter os melhores resultados.

    Para obter mais informações sobre como publicar pacotes, consulte [como publicar um pacote usando o console de gerenciamento](how-to-publish-a-package-by-using-the-management-console-50.md).

3.  Implantar pacotes nos computadores cliente.

4.  Converta os pontos de extensão, conforme necessário. Para obter mais informações, consulte os seguintes recursos:

    -   [Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [Como converter um pacote criado em uma versão anterior do App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Teste se seus pacotes do App-V 5,0 foram bem-sucedidos e, em seguida, remova os pacotes do 4,6. Para verificar o estado do usuário dos seus computadores cliente, recomendamos que você use a [virtualização da experiência do usuário](https://technet.microsoft.com/library/dn458947.aspx) ou outra ferramenta de gerenciamento do ambiente do usuário.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Planejamento para a migração de uma versão anterior do App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Implantação do sequenciador e do cliente App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

 

 





