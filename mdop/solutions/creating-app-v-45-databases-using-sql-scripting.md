---
title: Criação de bancos de dados do App-V 4.5 usando scripts SQL
description: Criação de bancos de dados do App-V 4.5 usando scripts SQL
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c119f1d43a70cce04dd6151697318f7cf6a8d1f2
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910586"
---
# <a name="creating-app-v-45-databases-using-sql-scripting"></a>Criação de bancos de dados do App-V 4.5 usando scripts SQL


**Who essa solução se destina?** Profissionais de tecnologia da informação que gerenciam bancos de dados de Virtualização de Aplicativo (App-V) 4.5.

**Como este guia pode ajudá-lo?** Essa solução explica e documenta o procedimento para instalar o Microsoft Application Virtualization Server quando o administrador que está instalando não tem privilégios "sysadmin" para o SQL Server.

## <a name="overview"></a>Visão geral


Um dos desafios de instalar o Microsoft Application Virtualization 4.5 (App-V) é que o programa de instalação supõe que o usuário que está instalando os recursos do servidor não seja apenas um administrador de computador local, mas também tenha privilégios de administrador SQL no servidor SQL que hospedará o Data Store. Esse requisito se baseia no fato de que o banco de dados, bem como as funções e permissões apropriadas, são criados como parte da instalação. No entanto, na maioria das empresas, SQL servidores são gerenciados separadamente da equipe de infraestrutura que instalará o App-V. Esses requisitos de segurança tornarão difícil obter SQL administradores para dar direitos adequados ao administrador de infraestrutura que está instalando o App-V; da mesma forma, os SQL administradores não terão os privilégios necessários para instalar o produto para a equipe de infraestrutura.

Atualmente, um administrador que tenta a instalação do App-V deve ter SQL privilégios "sysadmin". Em versões anteriores do produto, a instalação permitia que os administradores SQL criam uma conta "sysadmin" temporária ou estavam presentes durante a instalação para fornecer credenciais com privilégios "sysadmin". Nesta versão, os scripts são fornecidos no produto lançado para que todos os administradores usem ao implementar sua infraestrutura.

Este whitepaper discute o cenário no qual a instalação precisará ser dividida em duas tarefas separadas: criar o banco de dados SQL e instalar os recursos do servidor App-V. Os SQL podem revisar os scripts de SQL e fazer modificações para resolver quaisquer conflitos com outros bancos de dados ou para dar suporte à integração com outras ferramentas. O resultado dos scripts é permitir que os administradores SQL preparar o banco de dados para que os administradores de infraestrutura não tenham que ter direitos avançados no servidor SQL. Isso é importante em ambientes onde as políticas de segurança proibiriam isso.

### <a name="sql-database-creation-process"></a>Banco de Dados SQL Processo de Criação

Os scripts SQL permitem que os administradores SQL criem o banco de dados necessário e também configurar os privilégios para que os administradores do App-V instalem e gerenciem o ambiente com êxito. As etapas para concluir essas tarefas são listadas posteriormente neste documento.

Esse processo separa as ações de criação e configuração do banco de dados da instalação real do App-V.

**Informações a serem fornecidas aos SQL administradores**

-   Nome do grupo AD que será do administrador do App-V

-   Nome do servidor em que o Servidor de Gerenciamento do App-V será instalado

**Informações a serem retornadas aos administradores de infraestrutura**

-   Nome do servidor de banco de dados ou instância e o nome do banco de dados do App-V

Depois que o banco de dados tiver sido preparado, os administradores do App-V poderão executar a instalação do App-V sem SQL privilégios de administrador.

### <a name="using-the-sql-setup-scripts"></a>Usando os scripts SQL de instalação

**Requisitos**

A seguir está uma lista de requisitos para usar os scripts localizados na pasta support\\createdb na raiz do local de extração selecionado.

-   Os scripts devem ser copiados para um local de gravação no computador onde serão executados (certifique-se de remover o atributo somente leitura desses scripts depois de serem copiados) e as ferramentas de cliente do SQL devem ser carregadas nesse computador (osql só é necessário para executar os arquivos em lotes de exemplo no computador local).

-   O SQL Server deve dar suporte Windows Autenticação.

-   Verifique se a instância SQL Server e o serviço SQL agente estão sendo executados.

-   Faça logoff com uma conta de domínio que é SQL administrador (sysadmin) no computador onde os scripts serão feitos.

Os scripts são executados sob as credenciais de domínio do usuário conectado.

**Criação de banco de dados usando SQL scripts**

**Tarefas a serem executadas SQL administradores:**

1.  Copie os scripts contidos na pasta support\\createdb da raiz do local de extração selecionado para o computador onde os scripts serão executados. Os arquivos a seguir são necessários para que os scripts sejam executados corretamente e devem ser chamados na ordem apresentada abaixo.

    -   database.sql

    -   roles.sql

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

2.  Revise e modifique, se necessário, o `database.sql` arquivo. As configurações padrão nomearão o banco de dados "APPVIRTDB".

    -   Se necessário, substitua instâncias `APPVIRTDB` de pelo que será `database name` usado.

    -   Modifique a propriedade no script com o caminho apropriado para o SQL Server `FILENAME` onde o banco de dados será criado.

3.  Revise e modifique, se necessário, o arquivo usado `database name [APPVIRTDB]` `roles.sql` no arquivo database.sql.

****

### <a name="example-of-how-to-automate-the-process-using-batch-files"></a>Exemplo de como automatizar o processo usando arquivos em lotes

Se usado, os dois arquivos em lotes de exemplo fornecidos executarão os SQL scripts da seguinte maneira:

1.  **Create\_schema.bat (1)**

    -   database.sql

    -   roles.sql

2.  **Create\_tables.bat (2)**

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

**Observação**  
Considerações cuidadosas ao modificar os scripts devem ser tomadas e devem ser feitas apenas por alguém com o conhecimento apropriado. Além disso, dos arquivos de exemplo apresentados apenas os seguintes devem ser alterados: **create\_schema.bat**, **create\_tables.bat**, **database.sql**e **roles.sql**. Todos os outros arquivos não devem ser modificados de forma alguma, pois isso pode fazer com que o banco de dados seja criado incorretamente, o que levará à falha dos serviços do App-V a serem instalados.



Os dois arquivos em lotes de exemplo devem ser colocados no mesmo diretório para o qual o restante SQL scripts foram copiados no computador.

1.  Execute o ** arquivo **create\_schema.batexemplo para criar o banco de dados. Esse script levará vários segundos para ser concluído e não deve ser interrompido.

    -   Execute o arquivo create schema.bat do diretório para o qual ele foi copiado. Sintaxe é: `SQLSERVERNAME` "Create\_schema.bat"

        ![AppV46SQLcreatebat.](images/appv46sqlcreatebat.bmp)

    -   Se esse script falhar durante a criação do novo banco de dados "APPVIRTDB", verifique o log conforme indicado para corrigir o problema. Será necessário excluir o banco de dados criado com uma execução parcial dos scripts para garantir que as tentativas subsequentes funcionem corretamente.

2.  Execute o `create_tables.bat` arquivo para criar as tabelas no banco de dados. Esse script levará vários segundos para ser concluído e não deve ser interrompido.

    -   Execute o create\_tables.bat do diretório onde ele foi copiado. Sintaxe é: `SQLSERVERNAME DBNAME` "create\_tables.bat"

        ![app-v 4.6 sql create\-table.bat.](images/appv46sqlcreate-tablebat.gif)

        Se o script falhar durante a criação das tabelas, verifique o log conforme indicado para corrigir o problema. Será necessário excluir o banco de dados e executar create\_schema.bat antes de tentar executar o arquivo create\_tables.bat em todas as tentativas subsequentes.

### <a name="setting-permissions-on-the-app-v-database"></a>Definindo permissões no banco de dados do App-V

As contas a seguir precisarão ser criadas no servidor SQL com permissões e funções específicas para o novo banco de dados para a instalação, implantação e administração contínua do ambiente App-V.

-   Crie um logon para o grupo de administradores do App-V no SQL Server e o banco de dados APPVIRTDB para os "administradores de domínio\\App-V" (onde "domínio" e "Administradores do App-V" serão alterados para refletir seu próprio ambiente) e adicioná-los à função de banco de dados SFTAdmin e SFTEveryone.

    ![permissões e funções do conjunto de scripts sql do app-v 4.6.](images/appv46sqlscriptsetpermsroles.gif)

-   Conceda a esse grupo permissão "EXIBIR QUALQUER DEFINIÇÃO" no nível global (Isso permite que o processo de instalação do Microsoft Application Virtualization Management Server verifique se o logon do Servidor de Gerenciamento já existe). Em MS-SQL 2005 e acima restrições de acesso aos metadados contidos em master.db foram adicionadas. O usuário criado na etapa anterior, por padrão, não terá os direitos necessários para a instalação do servidor. Abra as propriedades do logon criado anteriormente, Propriedades de Logon- &gt; Securables. Adicione a instância banco de dados e habilita "GRANT" para "Exibir qualquer definição" conforme mostrado na captura de tela abaixo.

    ![app-v 4.6 sql script grant perm for view any def.](images/appv46sqlscriptviewanydef.gif)

-   Adicione uma função à tabela ROLE\_ASSIGNMENTS para o logon criado na etapa anterior para permitir que os administradores do App-V acessem o Console de Gerenciamento de Virtualização de Aplicativos, com a função = "ADMIN" e group\_ref = "domain\\App-V Admins" (onde "domínio" e "Administradores do App-V" serão alterados para refletir seu próprio ambiente).

    ![atribuição de função de script sql do app-v 4.6.](images/appv46sqlscriptroleassign.gif)

-   Crie logon para SQL Server e banco de dados do App-V para o Servidor de Gerenciamento. Essa conta é usada pelo Servidor de Gerenciamento de Virtualização de Aplicativos da Microsoft para se conectar ao armazenamento de dados e é responsável por atender às solicitações do cliente para aplicativos transmitidos. Há duas opções, dependendo de onde o SQL Server e o Servidor de Gerenciamento devem ser instalados:

    1.  Se o Servidor de Gerenciamento e SQL Server serão instalados no mesmo computador, adicione um logon para NT AUTHORITY\\NETWORK SERVICE e adicione-o às funções de banco de dados SFTUser e SFTEveryone.

    2.  Se o Servidor de Gerenciamento e o SQL Server devem ser instalados em computadores diferentes, adicione um logon para "domain\\App-V Server Name$" (onde "Nome do Servidor do App-V" é o nome do servidor onde o Servidor de Gerenciamento do App-V será instalado) e adicione-o às funções de banco de dados SFTUser e SFTEveryone.

-   Abra a janela de consulta na janela SQL e execute o seguinte SQL:

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Onde o APPVIRTDB é o nome do Banco de Dados do App-V criado no SQL Server na etapa anterior, e o usuário que fará a instalação do servidor App-v precisa ser membro de "domain\\App-V Admins" (onde "domínio" e "Administradores do App-V" serão alterados para refletir seu próprio ambiente).

### <a name="tasks-to-be-performed-by-the-infrastructure-administrators"></a>Tarefas a serem executadas pelos administradores de infraestrutura

1.  O administrador no grupo "Administradores do App-V" deve instalar o App-V.

    Use informações dos administradores SQL para selecionar o SQL Server e o banco de dados criado nas etapas anteriores.

2.  O administrador no grupo "Administradores do App-V" faz logon no Console de Gerenciamento de Virtualização de Aplicativos e exclui os seguintes objetos do Console de Gerenciamento.

    **Aviso**  
    Isso é necessário à medida que a instalação tradicional preenche determinados registros no banco de dados que não são preenchidos se você executar a instalação em um banco de dados já existente. Exclua os seguintes objetos:

    -   Em "Grupos de Servidores", "Grupo de Servidores Padrão", exclua "Servidor de Gerenciamento de Virtualização de Aplicativos"

    -   Em "Grupos de Servidores", exclua "Grupo de Servidores Padrão"

    -   Em "Políticas de Provedor", exclua "Provedor Padrão"



3.  Em seguida, o administrador no grupo de administradores do App-V deve criar:

    -   Em "Políticas de Provedor", crie uma Nova Política de Provedor

    -   Criar um "Grupo de Servidores Padrão"

        **Observação**  
        Você deve criar um grupo "Servidor Padrão", mesmo que não seja usado. O instalador de servidor procura apenas o "Grupo de Servidores Padrão" ao tentar adicionar o servidor.  Se não houver nenhum "Grupo de Servidores Padrão", a instalação falhará. Se você planeja usar grupos de servidores diferentes do padrão, é necessário manter o "Grupo de Servidores Padrão" se você planeja adicionar servidores de gerenciamento do App-V subsequentes à sua infraestrutura.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <a name="conclusion"></a>Conclusão


Em conclusão, as informações neste documento permitem que um administrador trabalhe com os administradores SQL para desenvolver um caminho de implantação que funcione para as divisões administrativas e de segurança em uma organização. Depois de ler este documento e testar as tarefas documentadas, um administrador deve estar pronto para implementar sua infraestrutura do App-V nesse tipo de ambiente.









