---
title: Solução de problemas de atualizações do AGPM
description: Solução de problemas de atualizações do AGPM
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797287"
---
# Solução de problemas de atualizações do AGPM

Esta seção lista alguns problemas comuns que você pode encontrar ao atualizar seu servidor de gerenciamento de política de grupo (AGPM) avançado para uma versão mais recente (por exemplo, AGPM 4,0 para AGPM 4,3). Para diagnosticar problemas não listados aqui, talvez seja útil exibir o [AGPM de solução de problemas](troubleshooting-agpm-agpm40.md) ou um administrador do AGPM (controle total) para usar o log e o rastreamento. Para obter mais informações, consulte [configurar log e rastreamento](configure-logging-and-tracing-agpm40.md).

## Quais são os problemas que você está tendo?

-   [Falha ao gerar um relatório de diferença de GPO HTML (código de erro 80004003)](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a>Falha ao gerar um relatório de diferença de GPO HTML (código de erro 80004003)

-   **Causa**: você instalou o pacote de atualização do AGPM com uma conta incorreta.

-   **Solução**: você precisará ser um administrador do AGPM para corrigir esse problema.
    
    -   Verifique se você conhece o nome de usuário & senha de sua **conta de serviço do AGPM**.

    -   Faça logon no seu servidor do AGPM de forma interativa como sua conta de serviço do AGPM.
        
        -   Isso é extremamente importante, pois a instalação falhará se você usar uma conta diferente.

    -   Desligue o serviço do AGPM.
    
    -   Instale o hotfix necessário.
    
    -   Conecte-se ao AGPM usando um cliente do AGPM para testar se seus relatórios de diferença estão funcionando agora.
    
## Instalar o pacote de hotfix 1 para o gerenciamento avançado de política de grupo da Microsoft 4,0 SP3
    
**Problema corrigido neste hotfix: o**AGPM não pode gerar relatórios de diferença quando controla ou gerencia novos objetos de política de grupo (GPOs).

**Como obter esta atualização**: Instale a versão mais recente do Microsoft Desktop Optimization Pack ([versão de serviço de março de 2017](https://www.microsoft.com/download/details.aspx?id=54967)). Consulte [KB 4014009](https://support.microsoft.com/help/4014009/) para obter mais informações.

Mais especificamente, você pode optar por baixar somente o primeiro arquivo, `AGPM4.0SP1_Server_X64_KB4014009.exe` a partir da lista apresentada após pressionar o botão baixar.
      
O link download para o pacote Microsoft Desktop Optimization Pack (versão de manutenção de março de 2017) pode ser encontrado [aqui](https://www.microsoft.com/download/details.aspx?id=54967).
      
      
## Link de referência
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
