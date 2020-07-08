---
title: Como determinar o estado de criptografia BitLocker de computadores perdidos
description: Como determinar o estado de criptografia BitLocker de computadores perdidos
author: dansimp
ms.assetid: 9440890a-9c63-463b-9113-f46071446388
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9b977b20ecf219830609c3b1f646a29e6678448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799443"
---
# Como determinar o estado de criptografia BitLocker de computadores perdidos


O Microsoft BitLocker Administration and Monitoring (MBAM) permite que você determine o último status de criptografia do BitLocker conhecido de computadores perdidos ou roubados. Use o procedimento a seguir para determinar se os volumes foram criptografados em computadores que não estão mais em sua posse.

**Determinar o último estado de criptografia do BitLocker conhecido do computador**

1.  Abra o site do MBAM.

    **Observação**  O endereço padrão do site MBAM é http://* &lt; ComputerName &gt; *. Use o nome de servidor totalmente qualificado para obter resultados de navegação mais rápidos.

     

2.  Selecione o nó do **relatório** no painel de navegação e selecione o **relatório de conformidade do computador**.

3.  Use os campos de filtro no painel à direita para restringir os resultados da pesquisa e, em seguida, clique em **Pesquisar**. Os resultados serão mostrados abaixo da sua consulta de pesquisa.

4.  Execute a ação adequada conforme determinado pela política para os dispositivos perdidos.

    **Observação**  A conformidade do dispositivo é determinada pelas políticas do BitLocker implantadas. Você deve verificar essas políticas implantadas quando está tentando determinar o estado de criptografia do BitLocker de um dispositivo.

     

## Tópicos relacionados


[Realizar o Gerenciamento do BitLocker com o MBAM](performing-bitlocker-management-with-mbam.md)

 

 





