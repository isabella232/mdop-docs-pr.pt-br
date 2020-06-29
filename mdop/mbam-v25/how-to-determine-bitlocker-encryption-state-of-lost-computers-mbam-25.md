---
title: Como determinar o estado de criptografia BitLocker de computadores perdidos
description: Como determinar o estado de criptografia BitLocker de computadores perdidos
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799479"
---
# Como determinar o estado de criptografia BitLocker de computadores perdidos


Use esse procedimento com o site de administração e monitoramento para determinar o seguinte:

-   O último status de criptografia BitLocker conhecido de computadores perdidos ou roubados

-   Se os volumes em um computador perdido ou roubado foram criptografados

Para concluir essa tarefa, você precisa ter acesso à área **relatórios** do site Administração e monitoramento. Para obter acesso a essa área, você deve receber a função de usuários de relatório MBAM. Você pode ter atribuído a essas funções nomes diferentes quando você as criou. Para obter mais informações, consulte [planejando para contas e grupos do MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**Observação**  A conformidade do dispositivo é determinada pelas políticas do BitLocker que sua empresa implantou. Você pode querer verificar suas políticas implantadas antes de tentar determinar o estado de criptografia do BitLocker de um dispositivo.

 

**Para determinar o último estado de criptografia do BitLocker conhecido de computadores perdidos**

1.  Abra um navegador da Web e navegue até o **site de administração e monitoramento**.

2.  No painel esquerdo, selecione **relatórios** para abrir a página relatórios.

3.  Selecione o **relatório de conformidade do computador**.

4.  Use os campos de filtro no painel à direita para restringir os resultados da pesquisa e, em seguida, clique em **Pesquisar**. Os resultados são mostrados na sua consulta de pesquisa.

5.  Execute a ação apropriada, conforme determinado pela política de dispositivos perdidos.



## Tópicos relacionados


[Realizando o gerenciamento do BitLocker com o MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Tem uma sugestão para o MBAM?
- Adicione ou vote em sugestões [aqui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas com o MBAM, use o [Fórum do TechNet do MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





