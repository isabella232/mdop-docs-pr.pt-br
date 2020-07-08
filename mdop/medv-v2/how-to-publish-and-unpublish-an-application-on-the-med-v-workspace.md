---
title: Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V
description: Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799969"
---
# Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V


Embora um aplicativo seja instalado em um espaço de trabalho do MED-V, você também pode ter que publicar o aplicativo antes que ele fique disponível para o usuário final. Por padrão, a maioria dos aplicativos é publicada no momento em que são instalados e os atalhos são criados e habilitados.

Em alguns casos, talvez você queira instalar aplicativos no espaço de trabalho do MED-V sem disponibilizá-los para o usuário final, por exemplo, software de verificação de vírus. Da mesma forma, há ocasiões em que você deseja publicar um aplicativo instalado no espaço de trabalho do MED-V que estava indisponível anteriormente para o usuário final. Por exemplo, talvez seja necessário publicar um aplicativo instalado se a instalação não criar automaticamente um atalho no menu **Iniciar** .

**Importante**  Se você publicar um aplicativo que não dê suporte a caminhos UNC, recomendamos mapear o aplicativo para uma unidade.

 

Você pode publicar ou cancelar a publicação de aplicativos em um espaço de trabalho do MED-V implantado executando uma das seguintes tarefas:

**Para publicar ou cancelar a publicação de um aplicativo instalado**

1.  Para publicar um aplicativo em um espaço de trabalho do MED-V implantado, copie um atalho para esse aplicativo para a pasta a seguir na máquina virtual:

    Menu C:\\Documents e Settings\\All Users\\Start

    Se for necessário, use a política de grupo ou um sistema ESD para implantar um script que copia o atalho do aplicativo para a pasta de menu todos os Users\\Start.

2.  Para cancelar a publicação de um aplicativo em um espaço de trabalho do MED-V implantado, exclua o atalho para esse aplicativo da seguinte pasta na máquina virtual:

    Menu C:\\Documents e Settings\\All Users\\Start

    Se for necessário, use a política de grupo ou um sistema ESD para implantar um script que exclui o atalho para esse aplicativo na pasta de menu todos os Users\\Start.

    **Observação**  Freqüentemente, o atalho é excluído automaticamente do menu **Iniciar** do computador host quando você desinstala o aplicativo. No entanto, em alguns casos, por exemplo, para um espaço de trabalho do MED-V configurado para todos os usuários de um computador compartilhado, talvez seja necessário excluir manualmente o atalho no menu **Iniciar** após a desinstalação do aplicativo. Para fazer isso, o usuário final pode clicar com o botão direito do mouse no atalho e selecionar **excluir**.

     

Para testar se o aplicativo foi publicado ou cancelado, verifique no espaço de trabalho do MED-V se o atalho correspondente está disponível ou não.

**Observação**  Os aplicativos incluídos no Windows XP SP3 e estão localizados na pasta do menu Iniciar da máquina virtual não são automaticamente publicados no host. Elas são controladas por configurações do registro que bloqueiam a publicação automática. Para obter mais informações, consulte [lista de exclusões de aplicativos PC virtual do Windows](windows-virtual-pc-application-exclude-list.md).

 

**Para publicar itens do painel de controle**

1.  Crie um atalho na máquina virtual em que o destino é o nome do item, como C:\\WINDOWS\\system32\\appwiz.cpl.

    O atalho deve ser criado ou movido para a pasta "%ALLUSERSPROFILE%\\Start Menu\\" ou uma de suas subpastas.

    O item será publicado no computador host no local correspondente na pasta do menu iniciar host.

2.  Inicie o atalho para o item no host.

**Cuidado**  Quando você cria o atalho, não especifique% SystemRoot% \\control.exe. Este aplicativo não será publicado porque está contido nas configurações do registro que bloqueiam a publicação automática.

 

**Como o MED-V manipula a publicação automática de aplicativos**

1.  Durante a publicação do aplicativo, o MED-V copia os atalhos da máquina virtual convidada para o computador host tentando corresponder à hierarquia de pastas existente no convidado. Fazendo isso, o MED-V copia atalhos do convidado para o host seguindo estas etapas:

    1.  O MED-V tenta localizar uma pasta em Start Menu\\Programs no computador host que tem o mesmo nome da pasta no convidado na qual o atalho reside.

    2.  Se não houver nenhuma pasta correspondente, o MED-V tentará localizar uma pasta na pasta do menu Iniciar do host com o nome da pasta no convidado em que o atalho reside.

    3.  Se não houver nenhuma pasta correspondente, o MED-V copiará o atalho para a pasta padrão no host, a pasta Start Menu\\Programs.

2.  Exemplo de processo de publicação do aplicativo:

    1.  Se um atalho de aplicativo for publicado na pasta Start Menu\\Programs\\AppShortcuts no Guest, o MED-V procurará no computador host por uma pasta AppShortcuts de início do Menu\\Programs\\ e, se for encontrado, copiará o atalho para essa pasta.

    2.  Se a pasta não for encontrada, o MED-V procura no computador host por uma pasta de início Menu\\AppShortcuts e, se for encontrado, copia o atalho para essa pasta.

    3.  Se a pasta não for encontrada, o MED-V copiará o atalho para a pasta Start Menu\\Programs.

**Observação**  Uma pasta já deve existir na pasta do menu Iniciar do computador host para o MED-V copiar o atalho para lá. O MED-V não cria a pasta, se ainda não existir.

 

## Tópicos relacionados


[Instalação e remoção de um aplicativo no espaço de trabalho da MED-V](installing-and-removing-an-application-on-the-med-v-workspace.md)

[Gerenciamento de atualizações de software para espaços de trabalho da MED-V](managing-software-updates-for-med-v-workspaces.md)

[Lista de exclusão do aplicativo Windows Virtual PC](windows-virtual-pc-application-exclude-list.md)

 

 





