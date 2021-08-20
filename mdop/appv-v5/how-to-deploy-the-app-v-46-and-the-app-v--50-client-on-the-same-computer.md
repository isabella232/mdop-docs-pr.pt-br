---
title: Como implantar o App-V 4.6 e o cliente App-V 5.0 no mesmo computador
description: Como implantar o App-V 4.6 e o cliente App-V 5.0 no mesmo computador
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.prod: w10
ms.openlocfilehash: f10f3d159c4724f3b486215b1169825bb029316d
ms.sourcegitcommit: 0132cd232b9c030820d95d91b71c4def0184400a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "11907224"
---
# <a name="how-to-deploy-the-app-v-46-and-the-app-v-50-client-on-the-same-computer"></a>Como implantar o App-V 4.6 e o cliente App-V 5.0 no mesmo computador

**Observação:** O App-V 4.6 saiu do suporte mainstream. O seguinte pressuporá que o cliente App-V 4.6 SP3 já está instalado.

Use as informações a seguir para instalar o cliente App-V 5.0 (preferencialmente, com os Service Packs e hotfixes mais recentes) e o cliente App-V 4.6 SP3 no mesmo computador. Para obter versões, requisitos e outras informações de planejamento com suporte, consulte [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).

**Para implantar o cliente App-V 5.0 e o cliente App-V 4.6 no mesmo computador**

1.  Instale o cliente App-V 5.0 SP3 no computador que está executando a versão app-V 4.6 do cliente. Para melhores resultados, recomendamos que você instale todas as atualizações disponíveis para o cliente App-V 5.0 SP3.

2.  Converta ou re-sequencia os pacotes gradualmente.

    -   Para converter os pacotes, use o conversor de pacote App-V 5.0 e converta os pacotes necessários para o formato de arquivo App-V 5.0 (**.appv**).

    -   Para sequenciar os pacotes de novo, considere usar a versão mais recente do Sequencer para melhores resultados.

    Para obter mais informações sobre pacotes de publicação, consulte [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).

3.  Implantar pacotes nos computadores cliente.

4.  Converta pontos de extensão, conforme necessário. Para obter mais informações, veja os seguintes recursos:

    -   [Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 convertido para todos os usuários em um computador específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [Como migrar pontos de extensão de um pacote do App-V 4.6 para um pacote do App-V 5.0 para um usuário específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [Como converter um pacote criado em uma versão anterior do App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Teste se os pacotes do App-V 5.0 são bem-sucedidos e remova os pacotes 4.6. Para verificar o estado do usuário de seus computadores clientes, recomendamos que você use a [Virtualização](https://technet.microsoft.com/library/dn458947.aspx) da Experiência do Usuário ou outra ferramenta de gerenciamento de ambiente de usuário.

    **Tem uma sugestão para o App-V?** Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema do App-V?** Use o [Fórum do TechNet do App-V.](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)

## <a name="related-topics"></a>Tópicos relacionados


[Planejamento para a migração de uma versão anterior do App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Implantação do sequenciador e do cliente App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

 

 





