---
title: Como iniciar, parar e reiniciar um espaço de trabalho do MED-V
description: Como iniciar, parar e reiniciar um espaço de trabalho do MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799729"
---
# Como iniciar, parar e reiniciar um espaço de trabalho do MED-V


**Para iniciar um espaço de trabalho do MED-V**

1.  Na área de notificação, clique com o botão direito do mouse no ícone do MED-V.

2.  No submenu, clique em **Iniciar espaço de trabalho**.

    -   Se houver vários espaços de trabalho do MED-V em execução no computador, a janela de **seleção do espaço de trabalho** será exibida.

        1.  Selecione um espaço de trabalho do MED-V.

        2.  Marque a caixa de seleção **iniciar o espaço de trabalho selecionado sem me perguntar** para ignorar esta janela da próxima vez que o cliente for iniciado e para abrir automaticamente o espaço de trabalho do MED-V selecionado.

        3.  Clique em **OK**.

    A janela **autenticação do espaço de trabalho inicial** é exibida.

    -   Se houver vários espaços de trabalho do MED-V no computador e se você tiver optado por usar um espaço de trabalho do MED-V especificado, a janela mostrada na figura a seguir será exibida.

        ![](images/medv-logon.gif)

    -   Se houver apenas um espaço de trabalho do MED-V no computador, a opção "Iniciar último espaço de trabalho usado" não estará disponível.

3.  Digite suas credenciais de usuário do domínio.

    **Observação**  Na primeira vez que um espaço de trabalho do MED-V for iniciado, o nome do usuário deve estar no seguinte formato: &lt; nome de usuário do nome do domínio &gt; \\ &lt; &gt; .

     

4.  Selecione **salvar minha senha** para salvar sua senha entre as sessões.

    **Observação**  Para habilitar o recurso salvar senha, o atributo EnableSavePassword deve ser definido como true no arquivo ClientSettings.xml. O arquivo pode ser encontrado na pasta *Servers\\Configuration Server\\* .

     

5.  Desmarque a caixa de seleção **Iniciar último espaço de trabalho usado** para escolher um espaço de trabalho do MED-V diferente.

6.  Clique em **OK**.

    Várias telas de status aparecem dependendo da configuração do espaço de trabalho do MED-V.

    A tela **inicial do espaço de trabalho** é exibida.

**Para reiniciar um espaço de trabalho do MED-V**

1.  Quando o cliente estiver em execução, na área de notificação, clique com o botão direito do mouse no ícone do MED-V.

2.  No submenu, clique em **reiniciar espaço de trabalho**.

    O espaço de trabalho do MED-V é reiniciado.

    -   Em um espaço de trabalho do MED-V persistente, a máquina virtual é desligada e reiniciada.

    -   Em um espaço de trabalho do MED-V reversível, a máquina virtual não desliga realmente; em vez disso, ele retorna ao seu estado original.

**Para parar um espaço de trabalho do MED-V**

1.  Na área de notificação, clique com o botão direito do mouse no ícone do MED-V.

2.  No submenu, clique em **parar espaço de trabalho**.

    O espaço de trabalho do MED-V é interrompido.

## Tópicos relacionados


[Como iniciar e fechar o cliente MED-V](how-to-start-and-exit-the-med-v-client.md)

 

 





