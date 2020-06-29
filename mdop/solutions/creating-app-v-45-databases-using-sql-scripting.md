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
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10799780"
---
# Criação de bancos de dados do App-V 4.5 usando scripts SQL


**Para quem esta solução se destina?** Profissionais de tecnologia da informação que gerenciam bancos de dados do Application Virtualization (App-V) 4,5.

**Como este guia pode ajudá-lo?** Esta solução explica e documenta o procedimento para instalar o servidor do Microsoft Application Virtualization quando a instalação do administrador não tem privilégios de "sysadmin" no SQL Server.

## Visão geral


Um dos desafios da instalação do Microsoft Application Virtualization 4,5 (App-V) é que o programa de instalação pressupõe que o usuário que está instalando os recursos do servidor não será apenas um administrador do computador local, mas também tenha privilégios de administrador do SQL no SQL Server que hospedarão o repositório de dados. Esse requisito se baseia no fato de que o banco de dados, bem como as funções e permissões adequadas, é criado como parte da instalação. No entanto, na maioria das empresas, o SQL Server é gerenciado separadamente da equipe de infraestrutura que instalará o App-V. Esses requisitos de segurança tornarão difícil que os administradores do SQL forneçam ao administrador de infraestrutura a instalação dos direitos adequados do App-V; da mesma forma, os administradores do SQL não terão os privilégios necessários para instalar o produto para a equipe de infraestrutura.

Atualmente, um administrador tentando instalar o App-V deve ter privilégios de "sysadmin" do SQL. Em versões anteriores do produto, a configuração permitiu para os administradores do SQL criarem uma conta temporária "sysadmin" ou estar presente durante a instalação para fornecer credenciais com privilégios "sysadmin". Nesta versão, os scripts são fornecidos no produto liberado para todos os administradores usarem ao implementar sua infraestrutura.

Este white paper descreve o cenário no qual a instalação precisará ser dividida em duas tarefas separadas: criar o banco de dados SQL e instalar os recursos do App-V Server. Os administradores do SQL podem revisar os scripts SQL e fazer modificações para resolver conflitos com outros bancos de dados ou para dar suporte à integração com outras ferramentas. O resultado dos scripts é permitir que os administradores do SQL Preparem o banco de dados para que os administradores de infraestrutura não precisem conceder direitos avançados no SQL Server. Isso é importante em ambientes em que as políticas de segurança proíberiam isso.

### Processo de criação de banco de dados SQL

Os scripts SQL permitem que os administradores do SQL criem o banco de dados necessário e também configurem os privilégios para os administradores do App-V instalarem e gerenciarem o ambiente com êxito. As etapas para concluir essas tarefas são listadas mais adiante neste documento.

Esse processo separa a criação do banco de dados e as ações de configuração da instalação real do App-V.

**Informações a serem fornecidas aos administradores do SQL**

-   Nome do grupo de anúncios que vai ser o administrador do App-V

-   Nome do servidor em que o servidor de gerenciamento do App-V será instalado

**Informações a serem retornadas para os administradores de infraestrutura**

-   Nome da instância ou do servidor de banco de dados e o nome do banco de dados App-V

Depois que o banco de dados for preparado, os administradores do App-V poderão executar a instalação do App-V sem privilégios de administrador do SQL.

### Usando os scripts de configuração do SQL

**Requisitos**

Veja a seguir uma lista de requisitos para usar os scripts localizados na pasta support\\createdb na raiz do local de extração selecionado.

-   Os scripts devem ser copiados para um local gravável no computador onde eles serão executados (certifique-se de remover o atributo somente leitura desses scripts após a cópia) e as ferramentas de cliente SQL devem ser carregadas nesse computador (o osql só é necessário para executar os arquivos em lotes de exemplo no computador local).

-   O SQL Server deve dar suporte à autenticação do Windows.

-   Verifique se a instância do SQL Server e o serviço do SQL Agent estão em execução.

-   Faça logon com uma conta de domínio que seja um administrador do SQL (sysadmin) no computador em que os scripts serão feitos.

Os scripts são executados sob as credenciais de domínio do usuário conectado.

**Criação de banco de dados usando scripts SQL**

**Tarefas a serem executadas pelos administradores do SQL:**

1.  Copie os scripts contidos na pasta support\\createdb da raiz do local de extração selecionado para o computador em que os scripts serão executados. Os arquivos a seguir são necessários para que os scripts sejam executados corretamente e devem ser chamados na ordem apresentada abaixo.

    -   Database. SQL

    -   Roles. SQL

    -   tabela \ _CODES. SQL

    -   funções \ _before \ _tables. SQL

    -   Tables. SQL

    -   functions. SQL

    -   views. SQL

    -   procedimentos. SQL

    -   triggers. SQL

    -   dados \ _codes. SQL

    -   dados \ _messages. SQL

    -   dados \ _defaults. SQL

    -   alertas \ _jobs. SQL

    -   DBVersion. SQL

2.  Revise e modifique, se necessário, o `database.sql` arquivo. As configurações padrão nomearão o banco de dados "APPVIRTDB".

    -   Se necessário, substitua as instâncias de `APPVIRTDB` pelo `database name` que serão usadas.

    -   Modifique a `FILENAME` propriedade no script com o caminho apropriado para o SQL Server em que o banco de dados será criado.

3.  Revise e modifique, se necessário, o `database name [APPVIRTDB]` `roles.sql` arquivo no arquivo que foi usado no arquivo Database. Sql.

****

### Exemplo de como automatizar o processo usando arquivos em lotes

Se usado, os dois arquivos em lotes de exemplo fornecidos executam os scripts SQL da seguinte maneira:

1.  **Create\_schema.bat (1)**

    -   Database. SQL

    -   Roles. SQL

2.  **Create\_tables.bat (2)**

    -   tabela \ _CODES. SQL

    -   funções \ _before \ _tables. SQL

    -   Tables. SQL

    -   functions. SQL

    -   views. SQL

    -   procedimentos. SQL

    -   triggers. SQL

    -   dados \ _codes. SQL

    -   dados \ _messages. SQL

    -   dados \ _defaults. SQL

    -   alertas \ _jobs. SQL

    -   DBVersion. SQL

**Observação**  
Uma consideração cuidadosa ao modificar os scripts deve ser feita e só deve ser feita por alguém com o conhecimento apropriado. Além disso, dos arquivos de exemplo apresentados somente o seguinte deve ser alterado: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**e **Roles. SQL**. Todos os outros arquivos não devem ser modificados da mesma forma que isso pode fazer com que o banco de dados seja criado incorretamente, o que levará à falha dos serviços do App-V a ser instalado.



Os dois arquivos em lotes de exemplo devem ser colocados no mesmo diretório em que o restante dos scripts SQL foram copiados para o computador.

1.  Execute o arquivo de exemplo **create\_schema.bat** para criar o banco de dados. Este script levará vários segundos para ser concluído e não deve ser interrompido.

    -   Execute o arquivo CREATE schema.bat do diretório em que foi copiado. A sintaxe é: "Create\_schema.bat `SQLSERVERNAME` "

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   Se esse script falhar durante a criação do novo banco de dados "APPVIRTDB", verifique o log indicado para corrigir o problema. Será necessário excluir o banco de dados que foi criado com uma execução parcial dos scripts para garantir que as tentativas subsequentes funcionem corretamente.

2.  Execute o `create_tables.bat` arquivo para criar as tabelas no banco de dados. Este script levará vários segundos para ser concluído e não deve ser interrompido.

    -   Execute o arquivo create\_tables.bat do diretório em que ele foi copiado. A sintaxe é: "create\_tables.bat `SQLSERVERNAME DBNAME` "

        ![create\-table.bat SQL do App-v 4,6](images/appv46sqlcreate-tablebat.gif)

        Se o script falhar durante a criação das tabelas, verifique o log conforme indicado para corrigir o problema. Será necessário excluir o banco de dados e executar o create\_schema.bat antes de tentar executar o arquivo create\_tables.bat em todas as tentativas subsequentes.

### Definindo permissões no banco de dados do App-V

As contas a seguir precisarão ser criadas no SQL Server com permissões e funções específicas para o novo banco de dados para instalação, implantação e administração contínua do ambiente App-V.

-   Crie um login para o grupo App-V Administrators no SQL Server e o banco de dados APPVIRTDB para "domain\\App-V admins" (em que "domínio" e "App-V administradores" serão alterados para refletir seu próprio ambiente) e adicioná-los à função de banco de dados SFTAdmin e SFTEveryone.

    ![App-v 4,6 o script SQL define permissões e funções](images/appv46sqlscriptsetpermsroles.gif)

-   Conceda a este grupo a permissão "exibir qualquer definição" no nível global (isso permite que o processo de instalação do servidor de gerenciamento do Microsoft Application Virtualization Verifique se o logon do servidor de gerenciamento já existe). Em MS-SQL 2005 e acima restrições de acesso aos metadados contidos em Master. DB foram adicionados. O usuário criado na etapa anterior não terá, por padrão, os direitos necessários para a instalação do servidor. Abra as propriedades do logon criado anteriormente, propriedades de logon- &gt; protegívels. Adicione a instância de banco de dados e habilite "GRANT" para "View any Definition", conforme mostrado na captura de tela abaixo.

    ![App-v 4,6 SQL script Grant Perm para View any def](images/appv46sqlscriptviewanydef.gif)

-   Adicione uma função à tabela ROLE \ _ASSIGNMENTS para o logon criado na etapa anterior para permitir que os administradores do App-V acessem o console de gerenciamento do Application Virtualization, com a função = "administrador" e grupo \ _ref = "domain\\App-V administradores" (em que "domínio" e "App-V administradores" serão alterados para refletir seu próprio ambiente).

    ![atribuição de função de script SQL do App-v 4,6](images/appv46sqlscriptroleassign.gif)

-   Crie um login para o SQL Server e o banco de dados App-V para o servidor de gerenciamento. Essa conta é usada pelo servidor de gerenciamento do Microsoft Application Virtualization para se conectar ao repositório de dados e é responsável por atender solicitações de cliente para aplicativos em fluxo. Há duas opções, dependendo de onde o SQL Server e o servidor de gerenciamento devem ser instalados:

    1.  Se o servidor de gerenciamento e o SQL Server forem instalados no mesmo computador, adicione um login para o serviço NT AUTHORITY\\NETWORK e adicione-o às funções de banco de dados SFTUser e SFTEveryone.

    2.  Se o servidor de gerenciamento e o SQL Server forem instalados em computadores diferentes, adicione um login para "domain\\App-V Server Name $" (onde "App-V Server Name" é o nome do servidor em que o servidor de gerenciamento do App-V será instalado) e adicione-o às funções de banco de dados SFTUser e SFTEveryone.

-   Abra a janela consulta na janela SQL e execute o seguinte SQL:

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Onde APPVIRTDB é o nome do banco de dados App-V criado no SQL Server na etapa anterior e o usuário que vai fazer a instalação do App-v Server precisa ser um membro de "domain\\App-V administradores" (em que "domínio" e "App-V administradores" será alterado para refletir seu próprio ambiente).

### Tarefas a serem realizadas pelos administradores de infraestrutura

1.  Administrador no grupo "App-V administradores" deve instalar o App-V.

    Use as informações dos administradores do SQL para selecionar o SQL Server e o banco de dados criados nas etapas anteriores.

2.  Administrador no grupo "App-V admins" conecta-se ao console de gerenciamento do Application Virtualization e exclui os seguintes objetos do console de gerenciamento.

    **Aviso**  
    Isso é necessário porque a configuração tradicional preenche determinados registros no banco de dados que não são preenchidos caso você execute a instalação em um banco de dados já existente. Exclua os seguintes objetos:

    -   Em "grupos de servidores", "grupo padrão do servidor", excluir "servidor de gerenciamento do Application Virtualization"

    -   Em "grupos de servidores", "excluir" grupo padrão do servidor "

    -   Em "políticas de provedor", "excluir" provedor padrão "



3.  Administrador no grupo App-V admins deve criar:

    -   Em "políticas de provedor", crie uma nova política de provedor

    -   Criar um "grupo de servidor padrão"

        **Observação**  
        Você deve criar um grupo de "servidor padrão" mesmo se não for usado. O instalador do servidor só procura o "grupo padrão do servidor" ao tentar adicionar o servidor.  Se não houver um "grupo de servidores padrão", a instalação não será bem-sucedida. Se você planeja usar grupos do servidor diferentes do padrão, é preciso manter o "grupo padrão do servidor" se planejar adicionar servidores de gerenciamento do App-V subsequentes à sua infraestrutura.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## Conclusão


Em conclusão, as informações neste documento permitem que um administrador trabalhe com os administradores do SQL para desenvolver um caminho de implantação que funcione para as divisões administrativas e de segurança de uma organização. Depois de ler este documento e testar as tarefas documentadas, um administrador deve estar pronto para implementar sua infraestrutura do App-V nesse tipo de ambiente.









