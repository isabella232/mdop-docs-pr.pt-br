---
title: Práticas recomendadas para o controle de versão
description: Práticas recomendadas para o controle de versão
author: dansimp
ms.assetid: 89067f6a-f7ea-4dad-999d-118284cf6c5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ed91408faeb8968175976382f9dd97d45becddb5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797478"
---
# Práticas recomendadas para o controle de versão


O gerenciamento avançado de política de grupo (AGPM) da Microsoft fornece controle de versão para objetos de política de grupo (GPOs) da mesma forma que o Microsoft Visual SourceSafe® fornece controle de versão para código-fonte. Os desenvolvedores podem usar o Visual SourceSafe para gerenciar várias versões de cada arquivo de origem. Os administradores de política de grupo podem usar o AGPM para fazer o mesmo para GPOs. Quando você usa o AGPM, os administradores de política de grupo devem estar cientes das práticas recomendadas que se aplicam a qualquer sistema de controle de versão:

-   **Data e hora:** O AGPM carimba cada versão de um GPO com a data e a hora. Para garantir que o histórico seja preciso, especialmente quando você edita GPOs em mais de um computador, verifique se cada computador sincroniza seu relógio com uma fonte de tempo autoritativa.

-   **Fazer check-in de GPOs quando terminar de editá-los:** É comum que os editores confiram os GPOs e esqueçam de verificá-los de volta ao arquivo morto. No entanto, isso pode impedir que outros administradores de política de grupo alterem o GPO. Sempre verifique os GPOs novamente no AGPM imediatamente quando terminar de editar.

-   **Salve as mudanças com frequência:** Ao editar um GPO, salve as alterações com frequência. A maioria dos editores verificam um GPO, fazem muitas alterações e, em seguida, verificamos o GPO no arquivo morto. Em vez disso, verifique o GPO em arquivar regularmente e, em seguida, dê uma olhada nele novamente. O detalhe pode ser tão pequeno quanto fazer check-in do GPO após alterar todas as configurações (não recomendado) ou fazer check-in do GPO depois de fazer grupos de alterações relacionadas. O resultado é um histórico melhor documentado para cada GPO que pode ajudar na solução de problemas.

-   **Implante GPOs com frequência:** Não deixe os GPOs novos e editados que ainda não foram implantados acumulados em números grandes no arquivo morto. Em vez disso, implante os GPOs novos e editados o mais rápido possível para que tenham um efeito mínimo sobre o ambiente de produção. Implantar vários GPOs novos e editados ao mesmo tempo pode prejudicar o ambiente de produção.

-   **Documentar a finalidade das alterações ao fazer check-in de GPOs:** Qualquer revisor pode comparar versões de um GPO para ver alterações específicas entre os dois. A documentação dessas alterações específicas não agrega valor. Em vez disso, documente a intenção e a finalidade de uma alteração em vez de documentar o que os revisores podem ver exibindo relatórios de diferença. Comentários sobre a versão devem adicionar valor ao relatório de comparação e ajudar um revisor a entender por que o editor alterou o GPO.

-   **Testar GPOs em um laboratório antes de implantá** -los: Implantar GPOs no ambiente de produção sem primeiro testá-los é arriscado. Em vez disso, teste os GPOs em um ambiente de laboratório vinculando-os a uma unidade organizacional que contém computadores de teste e usuários e verificando se eles funcionam corretamente. Depois de verificar cada GPO no laboratório, implante o GPO no ambiente de produção.

### Referências adicionais

-   [Guia operacional do Gerenciamento Avançado de Política de Grupo 3.0 da Microsoft](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





