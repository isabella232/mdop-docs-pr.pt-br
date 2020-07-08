---
title: Planejamento de alta disponibilidade com o App-V 5.0
description: Planejamento de alta disponibilidade com o App-V 5.0
author: dansimp
ms.assetid: 6d9a6492-23f8-465c-82e5-49c863594156
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebf586de7cae19d40d76c9c0c845f93e7bd9021b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796263"
---
# Planejamento de alta disponibilidade com o App-V 5.0


As configurações do sistema do Microsoft Application Virtualization 5,0 (App-V 5,0) podem tirar proveito das opções que mantêm um alto nível de serviço disponível.

Use as informações das seções a seguir para ajudá-lo a entender as opções de implantação do App-V 5,0 em uma configuração altamente disponível.

-   [Suporte para clustering do Microsoft SQL Server](#bkmk-sqlcluster)

-   [Suporte para balanceamento de carga de rede do IIS](#bkmk-iisloadbal)

-   [Suporte a servidores de arquivos em cluster ao executar o modo (SCS)](#bkmk-clusterscsmode)

-   [Suporte para espelhamento do Microsoft SQL Server](#bkmk-sqlmirroring)

-   [Suporte para o Microsoft SQL Server sempre ligado](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a>Suporte para clustering do Microsoft SQL Server


Você pode executar o banco de dados de gerenciamento do App-V e o banco de dados de relatórios em computadores que executam clusters do Microsoft SQL Server. No entanto, você deve instalar os bancos de dados usando scripts.

Para obter instruções, consulte [como implantar os bancos de dados do App-V usando scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).

## <a href="" id="bkmk-iisloadbal"></a>Suporte para balanceamento de carga de rede do IIS


Você pode usar o balanceamento de carga de rede dos serviços de informações da Internet (IIS) para configurar um ambiente altamente disponível para computadores que executam os serviços de gerenciamento, publicação e relatórios do App-V 5. x que são implantados pelo IIS.

Revise as informações a seguir para obter mais informações sobre como configurar o IIS e o balanceamento de carga de rede para computadores que executam sistemas operacionais Windows Server:

-   Fornece informações sobre como configurar os serviços de informações da Internet (IIS) 7,0.

    [Obtendo alta disponibilidade e escalabilidade-ARR e NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)

-   Configurando o Microsoft Windows Server

    [Balanceamento de carga de rede](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .

    Essas informações também se aplicam aos clusters de balanceamento de carga de rede (NLB) do IIS no Windows Server2008, no Windows Server2008R2 ou no Windows Server2012.

    **Observação**  A funcionalidade de balanceamento de carga de rede do IIS no Windows Server2012 geralmente é a mesma que no Windows Server2008R2. No entanto, alguns detalhes da tarefa são alterados no Windows Server2012. Para obter informações sobre novas maneiras de executar tarefas, consulte [tarefas comuns de gerenciamento e navegação no Windows server 2012 R2 Preview e no Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .

     

## <a href="" id="bkmk-clusterscsmode"></a>Suporte a servidores de arquivos em cluster ao executar o modo (SCS)


A execução do App-V 5,0 no modo de armazenamento de conteúdo de compartilhamento (SCS) com servidores de arquivos clusterizados é compatível.

As etapas a seguir podem ser usadas para habilitar essa configuração:

-   Configurar o App-V 5,0 para ser executado no modo SCS do cliente. Para obter mais informações sobre a configuração do modo SCS do App-V 5,0, consulte [como instalar o app-v 5,0 cliente para o modo de repositório de conteúdo compartilhado](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).

-   Configure o cluster de servidor de arquivos configurado no modo de dimensionamento do Microsoft Server2012 e no modo pré **2012** com uma rede SAN virtual.

As etapas a seguir podem ser usadas para validar a configuração:

1.  Adicione um pacote no servidor de publicação. Para obter mais informações sobre como adicionar um pacote, consulte [como adicionar ou atualizar pacotes usando o console de gerenciamento](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).

2.  Realize uma atualização de publicação no computador que executa o cliente App-V 5,0 e abra um aplicativo.

3.  Alternar os nós de cluster de opções de atualização de publicação mid e de fluxo contínuo para garantir que o failover funcione corretamente.

Revise as informações a seguir para obter mais informações sobre como configurar clusters de failover do Windows Server:

-   [Lista de verificação: criar um servidor de arquivos em cluster](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .

-   [Use volumes compartilhados de cluster em um cluster de failover do Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .

## <a href="" id="bkmk-sqlmirroring"></a>Suporte para espelhamento do Microsoft SQL Server


Usando o espelhamento do Microsoft SQL Server, no qual o banco de dados do servidor de gerenciamento do App-V 5,0 é espelhado usando duas instâncias do SQL Server, há suporte para bancos de dados do App-V 5,0 Management Server.

Revise as informações a seguir para obter mais informações sobre como configurar o espelhamento do Microsoft SQL Server:

-   [Como: preparar um banco de dados espelho para espelhamento (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Estabeleça uma sessão de espelhamento de banco de dados usando a autenticação do Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)

As etapas a seguir podem ser usadas para validar a configuração:

1.  Inicie uma sessão de espelhamento do Microsoft SQL Server.

2.  Selecione **failover** para designar uma nova instância mestra do SQL Server.

3.  Verifique se o servidor de gerenciamento do App-V 5,0 continua funcionando como esperado após o failover.

A cadeia de conexão no servidor de gerenciamento pode ser modificada para incluir o **parceiro de failover = &lt; &gt; Server2**. Isso só ajudará quando o principal no espelho tiver reprovado para o secundário e o computador executando o cliente App-V 5,0 estiver fazendo uma conexão nova (Diga após a reinicialização).

Use as etapas a seguir para modificar a cadeia de conexão para incluir o **parceiro de failover = &lt; &gt; Server2**:

**Importante**  Este tópico descreve como alterar o registro do Windows usando o editor do registro. Se você alterar o registro do Windows incorretamente, poderá causar sérios problemas que talvez exijam a reinstalação do Windows. Você deve fazer uma cópia de backup dos arquivos do registro (System. dat e User. dat) antes de alterar o registro. A Microsoft não pode garantir que os problemas que podem ocorrer quando você alterar o registro possam ser resolvidos. Altere o registro por sua conta e risco.

 

1.  Faça logon no servidor de gerenciamento e abra **regedit**.

2.  Navegue até **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **ManagementService**.

3.  Modifique o valor de **Gerenciamento \ _SQL \ _CONNECTION \ _STRING** com o **parceiro de failover = &lt; Server2 &gt; **.

4.  Reinicie o serviço de gerenciamento usando o console do IIS.

    **Observação**  O espelhamento de banco de dados está na lista de recursos de mecanismo de banco de dados substituídos do Microsoft SQL Server2012 devido ao recurso **AlwaysOn** disponível com o Microsoft SQL Server 2012.

     

Clique em qualquer um dos links a seguir para obter mais informações:

-   [Como: preparar um banco de dados espelho para espelhamento (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .

-   [Como: configurar uma sessão de espelhamento de banco de dados (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .

-   [Estabeleça uma sessão de espelhamento de banco de dados usando a autenticação do Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .

-   [Recursos de mecanismo de banco de dados preteridos no SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .

## <a href="" id="bkmk-sqlalwayson"></a>Suporte para a configuração AlwaysOn do Microsoft SQL Server


O banco de dados do aplicativo de gerenciamento do App-V 5,0 dá suporte a implantações em computadores que executam o Microsoft SQL Server com a configuração **sempre ativa** .

## Tópicos relacionados


[Planejando a implantação do App-V](planning-to-deploy-app-v.md)

 

 





