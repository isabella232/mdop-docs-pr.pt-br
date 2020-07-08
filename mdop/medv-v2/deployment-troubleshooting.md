---
title: Solução de problemas de implantação
description: Solução de problemas de implantação
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799164"
---
# Solução de problemas de implantação


Este tópico inclui informações para ajudá-lo a solucionar problemas de implantação na virtualização de área de trabalho do Microsoft Enterprise (MED-V) 2,0.

## Solucionando problemas na implantação do MED-V


O seguinte problema pode ocorrer ao implantar o MED-V. A solução ajuda a solucionar esse problema.

**Ocorrerão problemas se você estiver instalando o MED-V somente para o usuário atual.** O MED-V só oferece suporte à instalação do pacote do espaço de trabalho do MED-V, ao agente de host do MED-V e ao espaço de trabalho do MED-v para todos os usuários. A instalação para o usuário atual só causa falhas na instalação dos componentes e na configuração do espaço de trabalho do MED-V.

**Solução**

Nunca use a opção **ALLUSERS = ""** ao instalar os componentes do MED-V.

**O MED-V requer o uso exclusivo da pilha de virtualização.** Somente uma pilha de virtualização pode ser executada por vez em um computador. O computador virtual do Windows deve usar a pilha virtual e o MED-V depende do PC virtual do Windows. Portanto, se você tentar implantar ou usar o MED-V quando outros aplicativos estiverem em execução que usam a pilha virtual, o MED-V não pode ser executado ou ser instalado com êxito.

**Solução**

Feche todos os aplicativos que estejam sendo executados que usem a pilha de virtualização antes de instalar ou executar o MED-V.

**Os atalhos permanecem após a desinstalação.** Por padrão, quando você desinstala o MED-V, os atalhos do menu **Iniciar** do usuário final são removidos. No entanto, em determinadas situações, por exemplo, para usuários finais que estiverem executando perfis móveis, os atalhos para aplicativos publicados do MED-V permanecem no menu **Iniciar** do usuário final.

**Solução**

Para excluir manualmente os atalhos restantes no menu **Iniciar** , clique com o botão direito do mouse nos atalhos e, em seguida, clique em **remover**.

**Desabilitar a configuração da política de grupo da mensagem de logon no espaço de trabalho do MED-V.** Se a mensagem de logon do Windows XP estiver habilitada no espaço de trabalho do MED-V, o usuário final deverá fazer logon toda vez que quiser abrir um aplicativo virtual do MED-V. Isso cria uma experiência de usuário ruim.

**Solução**

Desabilite as seguintes configurações de política de grupo na máquina virtual do MED-V:

**Logon interativo: texto de mensagem para usuários tentando fazer logon**

**Logon interativo: Título da mensagem para usuários tentando fazer logon**

## Tópicos relacionados


[Solução de problemas de operações](operations-troubleshooting-medv2.md)

 

 





