---
title: Como desinstalar os componentes da MED-V
description: Como desinstalar os componentes da MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796147"
---
# Como desinstalar os componentes da MED-V


Em determinadas circunstâncias, talvez você queira desinstalar todos ou parte dos componentes do 2,0 da virtualização de área de trabalho do Microsoft Enterprise (MED-V) de sua empresa. Por exemplo, você solucionou todos os problemas de compatibilidade do sistema operacional do aplicativo ou deseja implantar um espaço de trabalho do MED-V diferente em sua empresa.

Geralmente, você pode configurar o sistema ESD (distribuição de software eletrônico) para desinstalar os componentes do MED-V usando um instalador baseado no Windows. Como alternativa, você pode desinstalar todos ou alguns componentes do MED-V manualmente.

**Importante**  Antes de desinstalar o agente de host do MED-V, você deve primeiro desinstalar qualquer espaço de trabalho do MED-V instalado.

 

Use os procedimentos a seguir para desinstalar os componentes do MED-V da sua empresa.

**Para desinstalar o MED-V usando um sistema de distribuição de software eletrônico**

1.  Use o sistema ESD para distribuir um script que invoque o uninstall.exe programa executável para cada espaço de trabalho do MED-V que você deseja desinstalar. O arquivo está localizado em C:\\ProgramData\\Microsoft\\Medv\\Workspace. Você pode definir um sinalizador para executar o programa de desinstalação executável silenciosamente para que os usuários finais não saibam a desinstalação.

2.  Crie um pacote para distribuir o arquivo de instalação do MED-V Host Agent para cada computador em que um espaço de trabalho do MED-V foi desinstalado. Configure o pacote para executar a desinstalação em modo silencioso.

O cliente ESD reconhece quando os novos pacotes estão disponíveis e começa a desinstalar os pacotes de acordo com a definição e os requisitos.

**Para desinstalar manualmente um espaço de trabalho do MED-V**

1.  No computador host, clique em **Iniciar**, clique em **painel de controle**e, em seguida, clique em **programas e recursos**.

2.  Na janela **programas e recursos** , selecione o espaço de trabalho do MED-V que você deseja remover e clique em **desinstalar**. (O espaço de trabalho do MED-V é chamado de "espaço de trabalho do MED-V- &lt; *espaço de trabalho \ _name* &gt; "). O &lt; _name assistente de configuração do *espaço de trabalho* &gt; **Setup Wizard** é aberto.

3.  No **Assistente de configuração**, clique em **Avançar**e, em seguida, clique em **remover**.

4.  Se preferir, marque a caixa de seleção para excluir o disco VHD mestre e os discos diferenciais criados pelo MED-V. Isso não é necessário, mas libera espaço em disco após o término da desinstalação.

5.  Clique em **remover**.

    **Observação**  Se o MED-V estiver sendo executado no momento, será exibida uma caixa de diálogo perguntando se você deseja desligá-la. Clique em **Sim** para continuar com a desinstalação. Clique em **não** para cancelar a desinstalação.

     

Como alternativa, você pode remover um espaço de trabalho do MED-V executando o `uninstall.exe` arquivo, normalmente localizado em C:\\ProgramData\\Microsoft\\Medv\\Workspace.

**Para desinstalar manualmente o agente de host do MED-V**

1.  No computador host do Windows 7, clique em **Iniciar**, clique em **painel de controle**e, em seguida, clique em **programas e recursos**.

2.  Na janela **programas e recursos** , selecione **agente de host MED-V**e clique em **desinstalar**.

    O Windows Installer remove o agente de host MED-V.

    **Observação**  Se você tentar desinstalar o agente de host do MED-V antes de desinstalar o espaço de trabalho do MED-V, será exibida uma caixa de diálogo que diz que você deve primeiro desinstalar o espaço de trabalho do MED-V. Clique em **OK** para continuar.

     

**Para desinstalar manualmente o pacote do espaço de trabalho do MED-V**

1.  No computador host, clique em **Iniciar**, clique em **painel de controle**e, em seguida, clique em **programas e recursos**.

2.  Na janela **programas e recursos** , selecione **pacote do espaço de trabalho do MED-V**e clique em **desinstalar**.

    O Windows Installer remove o pacote do espaço de trabalho do MED-V.

    **Observação**  Você pode desinstalar o pacote do espaço de trabalho do MED-V a qualquer momento, sem afetar qualquer espaço de trabalho do MED-V implantado.

     

## Tópicos relacionados


[Implantar os componentes da MED-V](deploy-the-med-v-components.md)

 

 





