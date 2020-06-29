---
title: Lista de exclusão do aplicativo Windows Virtual PC
description: Lista de exclusão do aplicativo Windows Virtual PC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799323"
---
# Lista de exclusão do aplicativo Windows Virtual PC


Em alguns casos, talvez você não queira que os aplicativos instalados no espaço de trabalho do MED-V sejam publicados no menu **Iniciar** do computador host. Você pode cancelar a publicação desses aplicativos seguindo as instruções em [como publicar e cancelar a publicação de um aplicativo no espaço de trabalho do MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md). No entanto, se o programa for atualizado automaticamente, ele também pode ser republicado automaticamente. Isso faz com que você tenha que cancelar a publicação do aplicativo novamente.

O Windows Virtual PC inclui um recurso conhecido como "lista de exclusões" que permite especificar determinados aplicativos instalados que você não deseja que sejam publicados no menu **Iniciar** do host. A "lista de exclusões" está localizada no registro convidado da chave HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList e lista os aplicativos que não são publicados no menu **Iniciar** do host. Você pode considerar a "lista de exclusões" como cancelar permanentemente a publicação dos aplicativos especificados, pois as atualizações automáticas dos aplicativos listados não farão com que eles sejam automaticamente republicados.

## Gerenciando aplicativos usando a lista de exclusões no PC virtual do Windows


****

1.  Abra o espaço de trabalho do MED-V em tela inteira.

    Para obter informações sobre como abrir o espaço de trabalho do MED-V no modo de tela inteira usando o kit de ferramentas de administração do MED-V, consulte [exibindo as configurações do espaço de trabalho do MED-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen). Ou você pode abri-lo manualmente em tela inteira clicando em **Iniciar**, em **todos os programas**, em **computador virtual do Windows**, clique em **PC virtual do Windows**e, em seguida, clique duas vezes no espaço de trabalho do MED-V.

2.  Na janela espaço de trabalho do Windows Virtual PC do MED-V, abra o editor do registro.

    Clique em **Iniciar**, clique em **executar**e digite regedit. Em seguida, clique em **OK**.

3.  No editor do registro, localize a chave do registro HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList

4.  Crie um novo valor do registro para o aplicativo instalado que você não deseja publicar no menu **Iniciar** do computador host. Por exemplo, se você quiser cancelar a publicação do programa publicado automaticamente do Microsoft Silverlight, siga estas etapas:

    1.  Com a chave do registro VPCVAppExcludeList realçada, clique em **Editar**, clique em **novo**e, em seguida, clique em **valor da cadeia de caracteres**.

    2.  Digite o nome do novo valor do registro. Por exemplo, para o Microsoft Silverlight, você pode inserir sllauncher.exe.

    3.  Clique duas vezes no novo valor do registro e insira os dados do valor.

        Os dados de valor são o caminho completo para o comando que você deseja cancelar a publicação. Para encontrar o caminho completo, clique com o botão direito do mouse no menu **Iniciar** do aplicativo que você não deseja publicar e, em seguida, clique em **Propriedades**. O caminho completo está listado na guia **atalho** em **destino**.

        Por exemplo, para o programa Microsoft Silverlight, o caminho completo pode ser "C:\\Arquivos de Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."

        **Importante**  Se aplicável, remova as aspas do caminho completo ao inseri-lo no campo dados do valor.

         

5.  Feche o editor do registro e reinicie a máquina virtual do espaço de trabalho do MED-V.

    O aplicativo ainda está instalado no espaço de trabalho do MED-V, mas agora é removido do menu **Iniciar** do computador host.

Você também pode republicar um aplicativo excluído no menu **Iniciar** do host excluindo o valor correspondente da chave VPCVAppExcludeList. Por exemplo, para republicar o Microsoft Silverlight, clique com o botão direito do mouse no valor do registro sllauncher.exe e selecione **excluir**.

## Tópicos relacionados


[Referência técnica da MED-V](technical-reference-for-med-v.md)

[Como publicar e cancelar a publicação de um aplicativo no espaço de trabalho da MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





