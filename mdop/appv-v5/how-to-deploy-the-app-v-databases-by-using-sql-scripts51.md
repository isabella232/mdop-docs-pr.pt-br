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
# <span data-ttu-id="5935c-103">Como implantar os bancos de dados do App-V usando scripts SQL</span><span class="sxs-lookup"><span data-stu-id="5935c-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>

<span data-ttu-id="5935c-104">Use as instruções a seguir para usar scripts SQL, em vez do Windows Installer, para:</span><span class="sxs-lookup"><span data-stu-id="5935c-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

- <span data-ttu-id="5935c-105">Instalar os bancos de dados do App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="5935c-105">Install the App-V 5.1 databases</span></span>
- <span data-ttu-id="5935c-106">Atualizar os bancos de dados do App-V para uma versão mais recente</span><span class="sxs-lookup"><span data-stu-id="5935c-106">Upgrade the App-V databases to a later version</span></span>

> [!NOTE]
> <span data-ttu-id="5935c-107">Se você já implantou o banco de dados do App-V 5,0 SP3, os scripts do SQL não são necessários para atualizar para o App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="5935c-107">If you have already deployed the App-V 5.0 SP3 database, the SQL scripts are not required to upgrade to App-V 5.1.</span></span>

## <span data-ttu-id="5935c-108">Como instalar os bancos de dados do App-V usando scripts SQL</span><span class="sxs-lookup"><span data-stu-id="5935c-108">How to install the App-V databases by using SQL scripts</span></span>

1. <span data-ttu-id="5935c-109">Antes de instalar os scripts de banco de dados, revise e mantenha uma cópia dos termos de licença do App-V.</span><span class="sxs-lookup"><span data-stu-id="5935c-109">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="5935c-110">Ao executar os scripts de banco de dados, você está concordando com os termos de licença.</span><span class="sxs-lookup"><span data-stu-id="5935c-110">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="5935c-111">Se não aceitá-los, você não deve usar este software.</span><span class="sxs-lookup"><span data-stu-id="5935c-111">If you do not accept them, you should not use this software.</span></span>
1. <span data-ttu-id="5935c-112">Copie o **appv\_server\_setup.exe** da mídia de versão do App-V para um local temporário.</span><span class="sxs-lookup"><span data-stu-id="5935c-112">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>
1. <span data-ttu-id="5935c-113">Em um prompt de comando, execute **appv\_server\_setup.exe** e especifique um local temporário para extrair os scripts de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5935c-113">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

    <span data-ttu-id="5935c-114">Exemplo: appv\_server\_setup.exe/layout c:\\ &lt; _caminho do local temporário_&gt;</span><span class="sxs-lookup"><span data-stu-id="5935c-114">Example: appv\_server\_setup.exe /layout c:\\&lt;_temporary location path_&gt;</span></span>

1. <span data-ttu-id="5935c-115">Navegue até o local temporário que você criou, abra a pasta **DatabaseScripts** extraída e revise o arquivo de Readme.txt apropriado para obter instruções:</span><span class="sxs-lookup"><span data-stu-id="5935c-115">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

    | <span data-ttu-id="5935c-116">Banco de dados</span><span class="sxs-lookup"><span data-stu-id="5935c-116">Database</span></span> | <span data-ttu-id="5935c-117">Localização do arquivo Readme.txt a ser usado</span><span class="sxs-lookup"><span data-stu-id="5935c-117">Location of Readme.txt file to use</span></span> |
    |--|--|
    | <span data-ttu-id="5935c-118">Banco de dados de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5935c-118">Management database</span></span> | <span data-ttu-id="5935c-119">Subpasta ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="5935c-119">ManagementDatabase subfolder</span></span> |
    | <span data-ttu-id="5935c-120">Banco de dados de relatórios</span><span class="sxs-lookup"><span data-stu-id="5935c-120">Reporting database</span></span> | <span data-ttu-id="5935c-121">Subpasta ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="5935c-121">ReportingDatabase subfolder</span></span> |

> [!CAUTION]
> <span data-ttu-id="5935c-122">O arquivo readme.txt na subpasta ManagementDatabase está desatualizado.</span><span class="sxs-lookup"><span data-stu-id="5935c-122">The readme.txt file in the ManagementDatabase subfolder is out of date.</span></span> <span data-ttu-id="5935c-123">As informações nos arquivos Leiame atualizados abaixo são as mais atuais e devem substituir as informações do Leiame fornecidas nas pastas do **DatabaseScripts** .</span><span class="sxs-lookup"><span data-stu-id="5935c-123">The information in the updated readme files below is the most current and should supersede the readme information provided in the **DatabaseScripts** folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5935c-124">O script InsertVersionInfo. SQL não é necessário para versões do banco de dados de gerenciamento do App-V posterior à App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="5935c-124">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="5935c-125">O script Permissions. SQL deve ser atualizado de acordo com a **etapa 2** no [artigo do KB 3031340](https://support.microsoft.com/kb/3031340).</span><span class="sxs-lookup"><span data-stu-id="5935c-125">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span> <span data-ttu-id="5935c-126">A **etapa 1** não é necessária para versões do App-v posteriores ao app-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="5935c-126">**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

## <span data-ttu-id="5935c-127">Conteúdo do arquivo README do banco de dados de gerenciamento atualizado</span><span class="sxs-lookup"><span data-stu-id="5935c-127">Updated management database README file content</span></span>

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

## <span data-ttu-id="5935c-128">Conteúdo do arquivo README do banco de dados atualizado</span><span class="sxs-lookup"><span data-stu-id="5935c-128">Updated reporting database README file content</span></span>

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

**<span data-ttu-id="5935c-129">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="5935c-129">Got an App-V issue?</span></span>** <span data-ttu-id="5935c-130">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5935c-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5935c-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5935c-131">Related topics</span></span>

[<span data-ttu-id="5935c-132">Implantação do servidor App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5935c-132">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="5935c-133">Como implantar o servidor do App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5935c-133">How to Deploy the App-V 5.1 Server</span></span>](how-to-deploy-the-app-v-51-server.md)
