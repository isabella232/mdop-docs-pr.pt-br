---
title: Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios
description: Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796396"
---
# Como instalar os bancos de dados de gerenciamento e relatórios em computadores separados dos serviços de gerenciamento e relatórios


Use o procedimento a seguir para instalar o servidor de banco de dados e o servidor de gerenciamento em computadores diferentes. O computador no qual você planeja instalar o servidor de banco de dados deve estar executando uma versão com suporte do Microsoft SQL ou haverá falha na instalação.

**Observação**  
Depois de concluir a implantação, o nome do **Microsoft SQL Server**, o **nome da instância** e o **nome do banco de dados** serão exigidos pelo administrador que está instalando o serviço para poder se conectar a esses bancos de dados.



**Para instalar o banco de dados de gerenciamento e o servidor de gerenciamento em computadores separados**

1.  Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo. Para iniciar a instalação do App-V 5,0 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador. Clique em **Instalar**.

2.  Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.

3.  Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).** Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**. Clique em **Avançar**.

4.  Na página **seleção de recursos** , selecione os componentes que você deseja instalar, marcando a caixa de seleção **banco de dados do servidor de gerenciamento** e clique em **Avançar**.

5.  Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.

6.  Na página inicial **criar novo banco de dados do servidor de gerenciamento**, aceite as seleções padrão, se necessário, e clique em **Avançar**.

    Se você estiver usando uma instância personalizada do SQL Server, selecione **usar uma instância personalizada** e digite o nome da instância.

    Se você estiver usando um nome de banco de dados personalizado, selecione **configuração personalizada** e digite o nome do banco de dados.

7.  Na página **criar novo banco de dados do servidor de gerenciamento** , selecione **usar um computador remoto**e digite a conta de computador remoto usando o seguinte formato: **Domain\\MachineAccount**.

    **Observação**  
    Se você planeja implantar o servidor de gerenciamento no mesmo computador, será necessário selecionar **usar este computador local**.



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. Para iniciar a instalação, clique em **instalar**.

**Para instalar o banco de dados de relatórios e o servidor de relatórios em computadores separados**

1.  Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo. Para iniciar a instalação do App-V 5,0 Server, clique com o botão direito do mouse e execute **appv\_server\_setup.exe** como administrador. Clique em **Instalar**.

2.  Na página de **introdução** , examine e aceite os termos de licença e clique em **Avançar**.

3.  Na página **usar o Microsoft Update para ajudar a manter seu computador seguro e atualizado** , para habilitar as atualizações da Microsoft, selecione **usar o Microsoft Update quando eu verificar se há atualizações (recomendado).** Para desabilitar o Microsoft Updates, selecione **não quero usar o Microsoft Update**. Clique em **Avançar**.

4.  Na página **seleção de recursos** , selecione os componentes que você deseja instalar, marcando a caixa de seleção **banco de dados do servidor de relatório** e clique em **Avançar**.

5.  Na página **local de instalação** , aceite o local padrão e clique em **Avançar**.

6.  Na página inicial **criar novo banco de dados do servidor de relatórios** , aceite as seleções padrão, se necessário, e clique em **Avançar**.

    Se você estiver usando uma instância personalizada do SQL Server, selecione **usar uma instância personalizada** e digite o nome da instância.

    Se você estiver usando um nome de banco de dados personalizado, selecione **configuração personalizada** e digite o nome do banco de dados.

7.  Na página **criar novo banco de dados do servidor de relatórios** , selecione **usar um computador remoto**e digite a conta de computador remoto usando o seguinte formato: **Domain\\MachineAccount**.

    **Observação**  
    Se você planeja implantar o servidor de relatórios no mesmo computador, será necessário selecionar **usar este computador local**.



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. Para iniciar a instalação, clique em **instalar**.

**Para instalar os bancos de dados de gerenciamento e relatórios usando scripts de banco de dados do App-V 5,0**

1.  Copie os arquivos de instalação do App-V 5,0 Server para o computador no qual você deseja instalá-lo.

2.  Para extrair os scripts do banco de dados do App-V 5,0, abra um prompt de comando e especifique o local onde os arquivos de instalação são salvos e execute o seguinte comando:

    **appv\_server\_setup.exe** **/layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.

3.  Após a extração ter sido completada, para acessar o arquivo Leiame de instruções e scripts de banco de dados do App-V 5,0:

    -   O Leiame de instruções e scripts de banco de dados de gerenciamento do App-V 5,0 estão localizados na seguinte pasta: banco de dados de gerenciamento de scripts de banco de **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Management Database**.

    -   O Leiame de instruções e scripts do banco de dados de relatórios do App-V 5,0 estão localizados na seguinte pasta: **InstallationExtractionLocation**de relatório de  \\  **scripts de banco de dados**do aplicativo  \\  **Reporting Database**.

4.  Para cada banco de dados, copie os scripts para um compartilhamento e modifique-os seguindo as instruções no arquivo readme.

    **Observação**  
    Para obter mais informações sobre como modificar os SIDs obrigatórios contidos nos scripts, consulte [como instalar os bancos de dados do App-V e converter os identificadores de segurança associados usando o PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).



5.  Execute os scripts no computador que está executando o Microsoft SQL Server.

    **Tem uma sugestão para o App-V**? Adicione ou vote em sugestões [aqui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados


[Implantação do App-V 5.0](deploying-app-v-50.md)









