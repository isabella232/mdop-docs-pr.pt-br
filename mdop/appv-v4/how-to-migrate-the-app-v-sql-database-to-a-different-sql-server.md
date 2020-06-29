---
title: Como migrar o banco de dados SQL do App-V para um SQL Server diferente
description: Como migrar o banco de dados SQL do App-V para um SQL Server diferente
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797052"
---
# Como migrar o banco de dados SQL do App-V para um SQL Server diferente


Os procedimentos a seguir descrevem em detalhes como migrar o banco de dados SQL do servidor de gerenciamento do Microsoft Application Virtualization (App-V) para um SQL Server diferente.

**Importante**  Esse procedimento requer que o serviço App-V Server seja interrompido e isso impedirá que os usuários finais usem seus aplicativos.

 

**Para fazer backup do banco de dados SQL do App-V**

1.  Abra o programa Services. msc e pare o serviço App-V Management Server em todos os servidores de gerenciamento que usam o banco de dados para ser migrado.

2.  No computador em que o banco de dados do App-V está localizado, abra o SQL Server Management Studio.

3.  Expanda o nó **bancos** de dados e localize o banco de dados App-V (o nome padrão é APPVIRT).

4.  Clique com o botão direito do mouse no banco de dados e selecione **tarefas** e, em seguida, selecione **fazer backup**.

5.  Verifique se o **modelo de recuperação** está definido como **simples** e se o **tipo de backup** está definido como **completo**. Altere as configurações do **conjunto de backup** e do **destino** se for necessário.

6.  Clique em **OK** para fazer backup do banco de dados. Depois que o backup for concluído com êxito, clique em **OK**.

7.  Abra o Windows Explorer e navegue até a pasta que contém o arquivo de backup do banco de dados, por exemplo, APPVIRT. Bak. Copie o arquivo de backup do banco de dados para o computador de destino que está executando o SQL Server.

**Para restaurar o banco de dados SQL do App-V para o computador de destino**

1.  No computador de destino, abra o SQL Server Management Studio, clique com o botão direito do mouse no nó **bancos** de dados e selecione **restaurar banco de dados**.

2.  Em **origem para restauração**, escolha **do dispositivo** e, em seguida, clique no botão "**...**" .

3.  Na caixa de diálogo **especificar backup** , verifique se a **mídia de backup** está definida como **arquivo** e clique em **Adicionar**.

4.  Selecione o arquivo de backup que você copiou do computador original que está executando o SQL Server e clique em **OK**.

5.  Clique em **OK** e, em seguida, clique para selecionar o conjunto de backup a ser restaurado.

6.  Em **destino para restauração**, clique na lista suspensa para o **banco de dados** e selecione o nome do banco de dados App-V, por exemplo, APPVIRT.

7.  Clique em **OK** para iniciar a restauração. Depois que a restauração for concluída com êxito, clique em **OK**.

8.  Expanda o nó **segurança** , clique com o botão direito do mouse em **logons** e selecione **novo logon**.

9.  No campo **nome de logon** , insira os detalhes da conta de serviço de rede para o servidor de gerenciamento App-V no formato de DOMAIN\\SERVERNAME $.

10. Na página **geral** , em **banco de dados padrão** , selecione o nome do banco de dados App-V, por exemplo, APPVIRT, e clique em **OK**.

11. Em **Selecione uma página**, clique para selecionar a página de **mapeamento de usuários** . Em **Usuários mapeados para este logon**, clique na caixa de seleção na coluna **mapa** para selecionar o banco de dados App-V.

12. Em **Associação de função de banco de dados para: &lt; &gt; appvdatabasename**, clique para selecionar **SFTEveryone** e, em seguida, clique em **OK**.

13. Verifique se o Firewall do Windows no novo computador que está executando o SQL Server está configurado para permitir que o servidor de gerenciamento do App-V acesse o sistema. Em **Ferramentas administrativas**, use o programa **Firewall do Windows com segurança avançada** para criar uma **regra de entrada** para a porta usada pelo SQL Server (o padrão é a porta 1433).

**Para migrar trabalhos do agente do SQL Server do App-V**

1.  No computador original que está executando o SQL Server, no SQL Server Management Studio, expanda o nó do **agente do SQL Server** e, em seguida, expanda o nó **Jobs** .

2.  Clique com o botão direito do mouse nos quatro trabalhos do App-V a seguir e selecione **trabalho de script como | CRIAR para | Arquivo**e salve cada script em uma pasta e dê um nome descritivo a cada script.

    -   **Banco de dados do SoftGrid (appvdbname) verificar histórico de uso**

    -   **Banco de dados do SoftGrid (appvdbname) fechar sessões órfãs**

    -   **Banco de dados do SoftGrid (appvdbname) reforçar o limite de tamanho**

    -   **Banco de dados do SoftGrid (appvdbname) monitorar o status do trabalho/alerta**

3.  Copie os quatro arquivos de script (. Sql) para o computador de destino que está executando o SQL Server e abra o SQL Server Management Studio.

4.  No Windows Explorer, clique com o botão direito do mouse em cada arquivo. SQL e clique em **executar**. Cada script será aberto em uma janela de consulta no SQL Server Management Studio. Clique em **executar** para cada script e verifique se cada um deles foi concluído com êxito.

5.  Atualize o nó **Jobs** no nó do **SQL Server Agent** e confirme se os quatro trabalhos foram criados com êxito.

**Para atualizar a configuração do servidor de gerenciamento do App-V**

1.  No servidor de gerenciamento App-V, modifique as seguintes chaves do registro:

    -   **SqlServerName**  =  &lt; newservername&gt;

    -   **SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;

    Em seguida, reinicie o serviço App-V Server.

2.  Navegue até localizar o arquivo SftMgmt. udl no diretório de instalação do App-V Management Server (o padrão é C:\\Arquivos de Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service). Clique com o botão direito do mouse no arquivo e selecione **abrir**.

3.  Na guia **conexão** , insira o nome do computador de destino que está executando o SQL Server e clique em **testar conexão**. Quando o teste for bem-sucedido, clique em **OK** e em **OK** novamente.

4.  Para versões do App-V Management Server anteriores ao 4,5 SP2, você deve atualizar as configurações de log de SQL. Em **grupos de servidores**, clique com o botão direito do mouse no grupo do servidor do qual o servidor é membro e selecione **Propriedades**.

5.  Na guia **log** , clique para selecionar a entrada do **banco de dados SQL** e, em seguida, clique em **Editar**.

6.  Altere o **nome do host DNS** para o nome do host do novo computador que está executando o SQL Server e clique em **OK**. Clique em **OK** duas vezes mais e reinicie o serviço App-V Server.

7.  Abra o console de gerenciamento do App-V, clique com o botão direito do mouse no nó **aplicativos** e selecione **Atualizar**. A lista de aplicativos deve ser exibida como antes.

 

 





