---
title: Como configurar o suporte para espelhamento do Microsoft SQL Server para o App-V
description: Como configurar o suporte para espelhamento do Microsoft SQL Server para o App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10797224"
---
# Como configurar o suporte para espelhamento do Microsoft SQL Server para o App-V


Você pode usar o procedimento a seguir para configurar seu ambiente do Microsoft Application Virtualization (App-V) para usar o espelhamento de banco de dados do Microsoft SQL Server. Configurar o espelhamento de banco de dados pode ajudar nos cenários de recuperação de desastres e failover. O App-V 4,5 SP2 dá suporte a todos os modos de espelhamento de banco de dados atualmente disponíveis para o Microsoft SQL Server 2005 e o SQL Server 2008.

**Observação**  
Esse procedimento foi escrito para administradores que estão familiarizados com a configuração e a configuração de bancos de dados e o espelhamento de banco de dados do SQL Server com o Microsoft SQL Server e, portanto, abrange apenas as configurações específicas que são exclusivas do App-V.



**Para configurar seu ambiente do App-V para usar o espelhamento de banco de dados do Microsoft SQL Server**

1.  Configure o espelhamento de banco de dados do SQL Server do banco de dados do App-V seguindo as práticas comerciais padrão para o espelhamento do banco de dados. Use os links a seguir para obter informações gerais sobre como implementar o espelhamento de banco de dados do Microsoft SQL Server:

    -   **Microsoft SQL 2005**–[Configurando o espelhamento do banco de dados](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)

    -   **Microsoft SQL 2008**–[Configurando o espelhamento do banco de dados](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)

    Além disso, você pode encontrar informações sobre as práticas recomendadas nas [práticas recomendadas de espelhamento de banco de dados e considerações de desempenho](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .

2.  Após a configuração do espelhamento, verifique se o banco de dados do App-V mostra um status de **(principal, sincronizado)** e se o banco de dados espelhado mostra um status de **(espelho, sincronizado/restauração)**. Resolva problemas de espelhamento antes de prosseguir para a próxima etapa. Para obter informações adicionais sobre como monitorar o status, consulte [monitorando o status do espelhamento](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .

3.  No computador SQL Server que hospeda o espelho do banco de dados do App-v, crie o logon do SQL Server para a conta de serviço de rede do servidor de gerenciamento do App-v usando o nome de conta de ** &lt; domínio &gt; \\ &lt; ManagementServerHostName &gt; $ **.

4.  Instale o cliente nativo do Microsoft SQL Server no servidor de gerenciamento do App-V e no computador que executa o serviço Web de gerenciamento do App-V, se instalado em um computador diferente. Se você planeja ter servidores de gerenciamento do App-V adicionais se conectarem ao banco de dados SQL espelhado para o balanceamento de carga, você deve instalar o Microsoft SQL Server Native Client nesses computadores também. Você pode baixar o Microsoft SQL Server Native Client da página [Microsoft SQL server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) no centro de download da Microsoft ( https://go.microsoft.com/fwlink/?LinkId=187479) .

5.  Verifique a chave de registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** e verifique se ela contém apenas o nome de host do SQL Server. Se ele incluir um nome de instância, por exemplo, *serverhostname\\instancename*, o nome da instância deve ser removido.

    **Importante**  
    O servidor de gerenciamento do App-V usa a biblioteca de rede TCP/IP para se comunicar com o SQL Server quando o espelhamento de banco de dados está habilitado e, portanto, os nomes de instância não podem ser usados. Em vez disso, os números das portas devem ser especificados nas chaves do registro.



6.  Verifique a chave de registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** e certifique-se de que ela contenha o número da porta usada para SQL no computador SQL Server. Se você estiver usando uma instância nomeada, esse valor chave deve ser definido como a porta usada para a instância nomeada.

7.  Crie a chave de registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** as REG \ _SZ e, em seguida, defina o valor para o nome do host do SQL Server que hospeda o espelho.

8.  Crie a chave de registro **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** como DWORD e, em seguida, defina o valor para o número da porta que é usado para SQL no computador que está executando o SQL Server para hospedar o espelho. Se você estiver usando uma instância nomeada para o espelho, esse valor chave deve ser definido como o número da porta que será usado para a instância nomeada.

9.  No computador que está executando o serviço Web de gerenciamento do App-V, configure o arquivo de texto do UDL (Universal Data Link). No diretório onde o App-V está instalado, clique duas vezes em **SftMgmt. udl** e especifique os seguintes valores:

    -   Na guia **provedor** , selecione o provedor OLE DB do **SQL Server Native Client 10,0**.

    -   Clique em **Avançar** para selecionar a guia **conexão** . Na caixa **nome do servidor** , digite o nome do servidor do SQL Server. Em seguida, selecione **usar a segurança integrada do Windows NT**. Por fim, clique na lista **Selecione o banco de dados**e, em seguida, selecione o nome do banco de dados App-V.

    -   Clique na guia **tudo** e selecione o **parceiro de failover**de entrada. Clique em **Editar valor**e insira o nome do servidor do SQL Server de failover. Clique em **OK**.

    **Importante**  
    O sistema App-V usa a autenticação Kerberos. Portanto, quando você configura o espelhamento do SQL no qual a autenticação Kerberos está habilitada no SQL Server e o serviço do SQL Server é executado em uma conta de usuário do domínio, você deve configurar manualmente um SPN. Para obter mais informações, consulte "quando o serviço SQL usa a conta baseada em domínio" no artigo [Configurando a administração do App-V para um ambiente distribuído](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .



10. Para verificar se o espelhamento do banco de dados está funcionando corretamente, teste o failover e confirme se o App-V Management Server continua funcionando corretamente.

    **Importante**  
    Continue com cuidado e siga as práticas comerciais padrão para garantir que as operações do sistema não sejam interrompidas em caso de falha.



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## Tópicos relacionados


[Como realizar tarefas administrativas no Application Virtualization Server Management Console](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









