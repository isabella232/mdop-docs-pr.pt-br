---
title: Reiniciar e redefinir um espaço de trabalho da MED-V
description: Reiniciar e redefinir um espaço de trabalho da MED-V
author: dansimp
ms.assetid: a959cdb3-a727-47c7-967e-e58f224e74de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48a644c2ed1668f87eb6e1a78521e780e8b783dd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799669"
---
# Reiniciar e redefinir um espaço de trabalho da MED-V


Durante a solução de problemas, às vezes você pode achar necessário reiniciar ou redefinir o espaço de trabalho do MED-V. Reiniciar o espaço de trabalho do MED-V é basicamente igual a reiniciar um computador físico. Redefinir o espaço de trabalho do MED-V reexecuta primeiro a configuração e exclui todos os dados armazenados na máquina virtual. Como todos os dados armazenados são excluídos, você normalmente só deve redefinir o espaço de trabalho do MED-V para resolver os problemas de solução de problemas mais sérios ou restaurar um espaço de trabalho do MED-V em funcionamento anterior para um estado de trabalho.

Para obter informações sobre como abrir o kit de ferramentas de administração do MED-V, consulte [solução de problemas do MED-v usando o kit de ferramentas de administração](troubleshooting-med-v-by-using-the-administration-toolkit.md).

**Reiniciando um espaço de trabalho do MED-V**

1.  Na janela do **Kit de ferramentas de administração do MED-v** , clique em reiniciar o **espaço de trabalho do MED-v**. Uma janela de diálogo é aberta, na qual você deve confirmar que deseja reiniciar o espaço de trabalho do MED-V.

2.  Clique em **reiniciar**.

    Todos os aplicativos publicados que estiverem em execução ou redirecionados sites que estiverem abertos serão fechados quando o espaço de trabalho do MED-V for reiniciado.

**Redefinir um espaço de trabalho do MED-V**

1.  Na janela do **Kit de ferramentas de administração do MED-v** , clique em **redefinir espaço de trabalho do MED-v**. Uma janela de diálogo é aberta, na qual você deve confirmar que deseja redefinir o espaço de trabalho do MED-V.

    **Aviso**  Redefinir o espaço de trabalho do MED-V faz com que a instalação seja novamente executada novamente e, assim, recarregar o disco rígido virtual original. Todos os dados armazenados no espaço de trabalho do MED-V desde a primeira vez em que a configuração foi executada originalmente serão excluídos.

     

2.  Clique em **Redefinir**.

    Todos os aplicativos publicados que estiverem em execução ou redirecionados sites que estiverem abertos serão fechados quando o espaço de trabalho do MED-V for redefinido.

## Tópicos relacionados


[Exibição e configuração de logs da MED-V](viewing-and-configuring-med-v-logs.md)

[Exibição de configurações do espaço de trabalho da MED-V](viewing-med-v-workspace-configurations.md)

 

 





