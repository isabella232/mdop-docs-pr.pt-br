---
title: Como instalar e configurar o aplicativo padrão
description: Como instalar e configurar o aplicativo padrão
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797111"
---
# Como instalar e configurar o aplicativo padrão


O aplicativo padrão é fornecido como parte da instalação e é copiado automaticamente para o servidor de gerenciamento do aplicativo Microsoft Application Virtualization (App-V) durante a instalação. Ele é usado para verificar se o servidor de gerenciamento foi instalado e configurado corretamente, mas deve ser publicado no cliente do Microsoft Application Virtualization (App-V) para que o usuário possa acessá-lo.

Use os procedimentos a seguir para publicar o aplicativo padrão e para transmiti-lo.

**Para publicar o aplicativo padrão**

1.  Faça logon no servidor de gerenciamento do App-V usando uma conta que seja membro do grupo de administradores do App-V especificado durante a instalação.

2.  No servidor de gerenciamento App-V, clique em **Iniciar**, clique em **Ferramentas administrativas**e clique em **console de gerenciamento do Application Virtualization**.

3.  No console de gerenciamento do App-V, clique em **ações**e, em seguida, clique em **conectar ao sistema do Application Virtualization**.

4.  Na página **Configurar conexão** , desmarque a caixa de seleção **usar conexão segura** .

5.  Na caixa **nome do host do serviço Web** , digite o nome de domínio totalmente qualificado (FQDN) do servidor de gerenciamento do App-V e clique em **OK**.

    **Observação**  Você também pode usar o **localhost** para o nome de host do serviço Web, se ele estiver instalado no servidor de gerenciamento.

     

6.  No console de gerenciamento do App-V, clique com o botão direito do mouse no nó do **servidor** e clique em **Opções do sistema**.

7.  Na guia **geral** , na caixa **caminho do conteúdo padrão** , digite o caminho UNC (Convenção Universal de nomenclatura) para a pasta de conteúdo que você criou no servidor durante a instalação; por exemplo, \ \ \ \ &lt; nome do servidor &gt; \\Content e, em seguida, clique em **OK**.

    **Importante**  Use o FQDN do nome do servidor para que o cliente possa resolver o nome corretamente.

     

8.  No console de gerenciamento do App-V, no painel de navegação, expanda o nó do **servidor** e clique em **aplicativos**.

9.  No painel de tópicos, clique em **aplicativo padrão**e, em seguida, no painel **ações** , clique em **Propriedades**.

10. Na caixa de diálogo **Propriedades** , ao lado da caixa **caminho do OSD** , clique em **procurar**.

11. Na caixa de diálogo **abrir** , digite o caminho UNC para a pasta de conteúdo que você criou no servidor durante a instalação; por exemplo, \ \ \ \ &lt; nome do servidor &gt; \\Content e pressione Enter. Você deve usar o nome do servidor real e não pode usar o **localhost** aqui.

    **Importante**  Certifique-se de que os valores nas caixas caminho do **OSD** e **caminho do ícone** estejam no formato UNC (por exemplo, \ \ \ \ &lt; nome do servidor &gt; \\Content\\DefaultApp.ico) e aponte para a pasta de conteúdo que você criou ao instalar o servidor. Não use **localhost** ou um caminho de arquivo contendo uma letra de unidade, como C:\\Arquivos de Files\\.. \\.. Disputa.

     

12. Selecione o arquivo DefaultApp. OSD e clique em **abrir**.

13. Repita as etapas anteriores para configurar o caminho do ícone.

14. Clique na guia **permissões de acesso** e confirme se o grupo usuários do App-V tem permissões de acesso ao aplicativo.

15. Clique na guia **atalhos** e, em seguida, clique em **publicar na área de trabalho do usuário**. Clique em **OK**.

16. Abra o Windows Explorer e localize o diretório de conteúdo.

17. Clique duas vezes no arquivo DefaultApp. OSD e abra-o com o bloco de notas.

18. Localize a linha que contém a marca **href** e altere-a para o código a seguir:

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    Ou, se você estiver usando RTSPs:

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. Feche o arquivo DefaultApp. OSD e salve as alterações.

**Para transmitir o aplicativo padrão**

1.  No computador em que o cliente App-V está instalado, faça logon como um usuário que seja membro do grupo usuários da virtualização de aplicativos especificado durante a instalação do servidor.

2.  Na área de trabalho, o atalho **aplicativo padrão do aplicativo virtualização de aplicativos** é exibido. Clique duas vezes no atalho para iniciar o aplicativo.

3.  Uma barra de status, exibida acima da área de notificação do Windows, relata que o aplicativo está iniciando. Se a inicialização do aplicativo for bem-sucedida, a tela de título do aplicativo padrão será exibida. Clique em **OK** para fechar a caixa de diálogo. Agora você confirmou que o sistema do App-V está funcionando corretamente.

## Tópicos relacionados


[Como configurar os servidores para a implantação baseada em servidor](how-to-configure-servers-for-server-based-deployment.md)

 

 





