---
title: Gerenciar impressoras em uma área de trabalho da MED-V
description: Gerenciar impressoras em uma área de trabalho da MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799808"
---
# Gerenciar impressoras em uma área de trabalho da MED-V


Na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0, o redirecionamento de impressoras fornece aos usuários finais uma experiência de impressão consistente entre a máquina virtual do MED-V e o computador host.

Este tópico fornece informações sobre como gerenciar a impressão em um espaço de trabalho do MED-V.

## Gerenciando impressoras em espaços de trabalho do MED-V


Na maioria dos casos, o MED-V manipula o redirecionamento da impressora automaticamente. Após o término da primeira vez, o MED-V identifica todas as impressoras de rede instaladas no host, recupera os drivers correspondentes do servidor de impressão de rede e, se encontrado, instala os drivers relevantes no espaço de trabalho do MED-V. Depois que todos os drivers forem encontrados e instalados, o MED-V reinicializará o espaço de trabalho do MED-V. Somente após a reinicialização do espaço de trabalho do MED-V, as impressoras do host estão presentes e estão disponíveis no convidado, em alguns minutos.

**Observação**  Se os aplicativos estiverem sendo executados no espaço de trabalho do MED-V, o usuário final será solicitado a permitir que o reinício continue ou adie-o até mais tarde. Se nenhum aplicativo estiver sendo executado, a reinicialização será automática e não será exibida para o usuário final.

 

Sempre que o MED-V é reiniciado, ele verifica se há novas impressoras instaladas no host e, se encontradas, recupera os drivers correspondentes do servidor de impressão de rede e os instala no convidado. Em seguida, o MED-V reinicia o espaço de trabalho do MED-V da mesma forma que quando a configuração foi concluída pela primeira vez.

**Importante**  Após a instalação dos drivers relevantes no convidado, as impressoras só se tornam visíveis no convidado após a reinicialização.

 

Se, a qualquer momento, não for possível localizar ou instalar um driver, ele deve ser instalado manualmente no convidado para que a impressora de rede esteja disponível para o usuário final.

A lista a seguir oferece algumas orientações adicionais:

O **MED-V gerencia apenas impressoras de rede**. Os drivers para impressoras instaladas localmente no host não são instalados automaticamente no convidado.

**O MED-V instala somente drivers de impressora, se encontrados no servidor de impressão**. Se não for encontrado, os drivers da impressora deverão ser instalados manualmente.

**As impressoras instaladas manualmente no convidado não estão acessíveis para o host**. Por padrão, o MED-V aceita apenas o redirecionamento de impressoras do convidado para o host.

**Aviso**  Se uma impressora é instalada manualmente no convidado e a mesma impressora é instalada posteriormente no host, o resultado é que a impressora é instalada duas vezes no convidado. Para evitar essa situação, uma prática recomendada do MED-V é gerenciar o redirecionamento de impressora apenas de uma maneira: desabilite o redirecionamento e instale as impressoras manualmente no convidado ou habilite o redirecionamento e não instale impressoras manualmente no convidado.

 

## Tópicos relacionados


[Gerenciar configurações de espaço de trabalho da MED-V](manage-med-v-workspace-settings.md)

 

 





