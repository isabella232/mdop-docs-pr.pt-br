---
title: Como implantar os bancos de dados do App-V usando scripts SQL
description: Como implantar os bancos de dados do App-V usando scripts SQL
author: dansimp
ms.assetid: 1183b1bc-d4d7-4914-a049-06e82bf2d96d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4695d105c1aa6732efb6b8ed05169cf29e7f972b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796416"
---
# Como implantar os bancos de dados do App-V usando scripts SQL

Use as instruções a seguir para usar scripts SQL, em vez do Windows Installer, para:

- Instalar os bancos de dados do App-V 5,1
- Atualizar os bancos de dados do App-V para uma versão mais recente

> [!NOTE]
> Se você já implantou o banco de dados do App-V 5,0 SP3, os scripts do SQL não são necessários para atualizar para o App-V 5,1.

## Como instalar os bancos de dados do App-V usando scripts SQL

1. Antes de instalar os scripts de banco de dados, revise e mantenha uma cópia dos termos de licença do App-V. Ao executar os scripts de banco de dados, você está concordando com os termos de licença. Se não aceitá-los, você não deve usar este software.
1. Copie o **appv\_server\_setup.exe** da mídia de versão do App-V para um local temporário.
1. Em um prompt de comando, execute **appv\_server\_setup.exe** e especifique um local temporário para extrair os scripts de banco de dados.

    Exemplo: appv\_server\_setup.exe/layout c:\\ &lt; _caminho do local temporário_&gt;

1. Navegue até o local temporário que você criou, abra a pasta **DatabaseScripts** extraída e revise o arquivo de Readme.txt apropriado para obter instruções:

    | Banco de dados | Localização do arquivo Readme.txt a ser usado |
    |--|--|
    | Banco de dados de gerenciamento | Subpasta ManagementDatabase |
    | Banco de dados de relatórios | Subpasta ReportingDatabase |

> [!CAUTION]
> O arquivo readme.txt na subpasta ManagementDatabase está desatualizado. As informações nos arquivos Leiame atualizados abaixo são as mais atuais e devem substituir as informações do Leiame fornecidas nas pastas do **DatabaseScripts** .

> [!IMPORTANT]
> O script InsertVersionInfo. SQL não é necessário para versões do banco de dados de gerenciamento do App-V posterior à App-V 5,0 SP3.

O script Permissions. SQL deve ser atualizado de acordo com a **etapa 2** no [artigo do KB 3031340](https://support.microsoft.com/kb/3031340). A **etapa 1** não é necessária para versões do App-v posteriores ao app-v 5,0 SP3.

## Conteúdo do arquivo README do banco de dados de gerenciamento atualizado

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************


Steps to install "AppVManagement" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
    Permissions.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the
    necessary SQL Server client software is installed and available from
    the specified location.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVManagement".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
##     in the file will not work.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. Run the following scripts against the "AppVManagement" database using the
    same account as above in order.

    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
##     Permissions.sql

```

## Conteúdo do arquivo README do banco de dados atualizado

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************

Steps to install "AppVReporting" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    UpgradeDatabase.sql
    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
    ScheduleReportingJob.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the 
    necessary SQL Server client software is installed and executable from
    the location you have chosen.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVReporting".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
    in the file will not work.

 3. Review the ScheduleReportingJob.sql file and make sure that the stored proc schedule
    time is acceptable. The default stored proc schedule time is at 12.01 AM (line 84). 
    If this time is not suitable, you can change this to a more suitable time. The time is
##     in the format HHMMSS.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. If upgrading the database, run UpgradeDatabase.sql This will upgrade database schema.

 2. Run the following scripts against the "AppVReporting" database using the
    same account as above in order.

    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
##     ScheduleReportingJob.sql

```

**Tem um problema com o App-V?** Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados

[Implantação do servidor App-V 5.1](deploying-the-app-v-51-server.md)

[Como implantar o servidor do App-V 5.1](how-to-deploy-the-app-v-51-server.md)
