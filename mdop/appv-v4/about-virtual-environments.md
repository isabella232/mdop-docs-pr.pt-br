---
title: Sobre ambientes virtuais
description: Sobre ambientes virtuais
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799063"
---
# Sobre ambientes virtuais


Os aplicativos virtuais são executados em ambientes virtuais. Os ambientes virtuais permitem que cada aplicativo seja executado em um servidor de desktop, laptop ou host de sessão de área de trabalho remota (host RDSession) sem instalação e alteração do sistema operacional do host. Cada aplicativo transporta suas próprias informações de configuração no ambiente virtual. Como resultado, muitos aplicativos são executados lado a lado com outros aplicativos no mesmo computador sem conflitos.

Os aplicativos virtuais são executados localmente, portanto, eles são executados com o desempenho completo, a funcionalidade e o acesso aos serviços locais que você esperaria de qualquer aplicativo instalado localmente.

Como cada aplicativo é executado em um ambiente virtual, os seguintes problemas são reduzidos:

-   Conflitos de aplicativos — em ambientes que não usam a virtualização de aplicativos, você deve testar exaustivamente cada aplicativo para garantir que ele não interfira em outros aplicativos instalados.

-   Teste de regressão — como o aplicativo não altera o sistema operacional subjacente, o teste de regressão extensa é eliminado.

-   Incompatibilidades de versão: versões diferentes do mesmo aplicativo podem ser executadas simultaneamente no mesmo computador.

-   Acesso multiusuário – aplicativos que não são executados no modo multiusuário e, portanto, não podem ser executados dentro de um host RDSession, agora podem fazê-lo e funcionar corretamente para vários usuários em um único host de RDSession.

-   Problemas de multilocação – duas instâncias do mesmo aplicativo que usam configurações diferentes podem ser executadas no mesmo computador ao mesmo tempo.

-   Siloing de servidor — a necessidade de muitos farms de servidores separados é eliminada.

Os ambientes virtuais incluem um registro virtual para cada aplicativo. As configurações de registro criadas por um aplicativo não podem ser vistas por outros aplicativos ou utilitários como o regedit. Em vez de copiar todo o registro, o registro virtual usa um método de *sobreposição* . Itens no registro do cliente podem ser lidos pelo aplicativo desde que uma cópia virtual desse item do registro não seja incluída no registro virtual. Todas as gravações de aplicativo no registro estão contidas no registro virtual.

Os ambientes virtuais também incluem um sistema de arquivos virtual e outros componentes virtuais, incluindo serviços virtuais e COM virtual.

## Tópicos relacionados


[Visão geral do Application Virtualization Client Management Console](application-virtualization-client-management-console-overview.md)

 

 





