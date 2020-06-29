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
# <span data-ttu-id="d0c85-103">Criação de bancos de dados do App-V 4.5 usando scripts SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-103">Creating App-V 4.5 Databases Using SQL Scripting</span></span>


**<span data-ttu-id="d0c85-104">Para quem esta solução se destina?</span><span class="sxs-lookup"><span data-stu-id="d0c85-104">Who is this solution intended for?</span></span>** <span data-ttu-id="d0c85-105">Profissionais de tecnologia da informação que gerenciam bancos de dados do Application Virtualization (App-V) 4,5.</span><span class="sxs-lookup"><span data-stu-id="d0c85-105">Information technology professionals who manage Application Virtualization (App-V) 4.5 databases.</span></span>

**<span data-ttu-id="d0c85-106">Como este guia pode ajudá-lo?</span><span class="sxs-lookup"><span data-stu-id="d0c85-106">How can this guide help you?</span></span>** <span data-ttu-id="d0c85-107">Esta solução explica e documenta o procedimento para instalar o servidor do Microsoft Application Virtualization quando a instalação do administrador não tem privilégios de "sysadmin" no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0c85-107">This solution explains and documents the procedure to install the Microsoft Application Virtualization Server when the administrator installing does not have “sysadmin” privileges to the SQL Server.</span></span>

## <span data-ttu-id="d0c85-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="d0c85-108">Overview</span></span>


<span data-ttu-id="d0c85-109">Um dos desafios da instalação do Microsoft Application Virtualization 4,5 (App-V) é que o programa de instalação pressupõe que o usuário que está instalando os recursos do servidor não será apenas um administrador do computador local, mas também tenha privilégios de administrador do SQL no SQL Server que hospedarão o repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="d0c85-109">One of the challenges of installing Microsoft Application Virtualization 4.5 (App-V) is that the install program assumes that the user installing the server features will not only be a local computer administrator, but also have SQL administrator privileges on the SQL server that will host the Data Store.</span></span> <span data-ttu-id="d0c85-110">Esse requisito se baseia no fato de que o banco de dados, bem como as funções e permissões adequadas, é criado como parte da instalação.</span><span class="sxs-lookup"><span data-stu-id="d0c85-110">This requirement is based on the fact that the database, as well as the appropriate roles and permissions, are created as part of the install.</span></span> <span data-ttu-id="d0c85-111">No entanto, na maioria das empresas, o SQL Server é gerenciado separadamente da equipe de infraestrutura que instalará o App-V.</span><span class="sxs-lookup"><span data-stu-id="d0c85-111">However, in most enterprises, SQL servers are managed separately from the infrastructure team who will be installing App-V.</span></span> <span data-ttu-id="d0c85-112">Esses requisitos de segurança tornarão difícil que os administradores do SQL forneçam ao administrador de infraestrutura a instalação dos direitos adequados do App-V; da mesma forma, os administradores do SQL não terão os privilégios necessários para instalar o produto para a equipe de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="d0c85-112">These security requirements will make it difficult to get SQL administrators to give the infrastructure administrator installing App-V adequate rights; similarly, the SQL administrators will not have the required privileges to install the product for the infrastructure team.</span></span>

<span data-ttu-id="d0c85-113">Atualmente, um administrador tentando instalar o App-V deve ter privilégios de "sysadmin" do SQL.</span><span class="sxs-lookup"><span data-stu-id="d0c85-113">Currently, an administrator attempting the installation of App-V must have SQL “sysadmin” privileges.</span></span> <span data-ttu-id="d0c85-114">Em versões anteriores do produto, a configuração permitiu para os administradores do SQL criarem uma conta temporária "sysadmin" ou estar presente durante a instalação para fornecer credenciais com privilégios "sysadmin".</span><span class="sxs-lookup"><span data-stu-id="d0c85-114">In previous versions of the product the setup allowed for the SQL administrators to either create a temporary “sysadmin” account or be present during installation to provide credentials with “sysadmin” privileges.</span></span> <span data-ttu-id="d0c85-115">Nesta versão, os scripts são fornecidos no produto liberado para todos os administradores usarem ao implementar sua infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="d0c85-115">In this release, scripts are provided in the released product for all administrators to use when implementing their infrastructure.</span></span>

<span data-ttu-id="d0c85-116">Este white paper descreve o cenário no qual a instalação precisará ser dividida em duas tarefas separadas: criar o banco de dados SQL e instalar os recursos do App-V Server.</span><span class="sxs-lookup"><span data-stu-id="d0c85-116">This whitepaper discusses the scenario in which the install will need to be divided into two separate tasks: creating the SQL database, and installing the App-V server features.</span></span> <span data-ttu-id="d0c85-117">Os administradores do SQL podem revisar os scripts SQL e fazer modificações para resolver conflitos com outros bancos de dados ou para dar suporte à integração com outras ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d0c85-117">The SQL administrators would be able to review the SQL scripts and make modifications to resolve any conflicts with other databases, or to support integration with other tools.</span></span> <span data-ttu-id="d0c85-118">O resultado dos scripts é permitir que os administradores do SQL Preparem o banco de dados para que os administradores de infraestrutura não precisem conceder direitos avançados no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0c85-118">The result of the scripts is to allow SQL administrators to prepare the database so that the infrastructure administrators do not have to be granted any advanced rights on the SQL server.</span></span> <span data-ttu-id="d0c85-119">Isso é importante em ambientes em que as políticas de segurança proíberiam isso.</span><span class="sxs-lookup"><span data-stu-id="d0c85-119">This is important in environments where security policies would prohibit this.</span></span>

### <span data-ttu-id="d0c85-120">Processo de criação de banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-120">SQL Database Creation Process</span></span>

<span data-ttu-id="d0c85-121">Os scripts SQL permitem que os administradores do SQL criem o banco de dados necessário e também configurem os privilégios para os administradores do App-V instalarem e gerenciarem o ambiente com êxito.</span><span class="sxs-lookup"><span data-stu-id="d0c85-121">The SQL scripts allow for SQL administrators to create the required database and also set up the privileges for the App-V administrators to successfully install and manage the environment.</span></span> <span data-ttu-id="d0c85-122">As etapas para concluir essas tarefas são listadas mais adiante neste documento.</span><span class="sxs-lookup"><span data-stu-id="d0c85-122">The steps for completing these tasks are listed later in this document.</span></span>

<span data-ttu-id="d0c85-123">Esse processo separa a criação do banco de dados e as ações de configuração da instalação real do App-V.</span><span class="sxs-lookup"><span data-stu-id="d0c85-123">This process separates the database creation and configuration actions from the actual App-V installation.</span></span>

**<span data-ttu-id="d0c85-124">Informações a serem fornecidas aos administradores do SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-124">Information to be provided to SQL administrators</span></span>**

-   <span data-ttu-id="d0c85-125">Nome do grupo de anúncios que vai ser o administrador do App-V</span><span class="sxs-lookup"><span data-stu-id="d0c85-125">Name of AD group that is going to be the App-V admin’s</span></span>

-   <span data-ttu-id="d0c85-126">Nome do servidor em que o servidor de gerenciamento do App-V será instalado</span><span class="sxs-lookup"><span data-stu-id="d0c85-126">Name of the server where App-V Management Server will be installed</span></span>

**<span data-ttu-id="d0c85-127">Informações a serem retornadas para os administradores de infraestrutura</span><span class="sxs-lookup"><span data-stu-id="d0c85-127">Information to be returned to the Infrastructure administrators</span></span>**

-   <span data-ttu-id="d0c85-128">Nome da instância ou do servidor de banco de dados e o nome do banco de dados App-V</span><span class="sxs-lookup"><span data-stu-id="d0c85-128">Name of the database server or instance and the name of the App-V database</span></span>

<span data-ttu-id="d0c85-129">Depois que o banco de dados for preparado, os administradores do App-V poderão executar a instalação do App-V sem privilégios de administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="d0c85-129">Once the database has been prepared, the App-V administrators can run the App-V installation without SQL administrator privileges.</span></span>

### <span data-ttu-id="d0c85-130">Usando os scripts de configuração do SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-130">Using the SQL Setup Scripts</span></span>

**<span data-ttu-id="d0c85-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0c85-131">Requirements</span></span>**

<span data-ttu-id="d0c85-132">Veja a seguir uma lista de requisitos para usar os scripts localizados na pasta support\\createdb na raiz do local de extração selecionado.</span><span class="sxs-lookup"><span data-stu-id="d0c85-132">The following is a list of requirements for using the scripts which are located in the support\\createdb folder at the root of the selected extract location.</span></span>

-   <span data-ttu-id="d0c85-133">Os scripts devem ser copiados para um local gravável no computador onde eles serão executados (certifique-se de remover o atributo somente leitura desses scripts após a cópia) e as ferramentas de cliente SQL devem ser carregadas nesse computador (o osql só é necessário para executar os arquivos em lotes de exemplo no computador local).</span><span class="sxs-lookup"><span data-stu-id="d0c85-133">Scripts must be copied to a writeable location on the computer where they will be run (be sure to remove the read only attribute from these scripts after they have been copied) and SQL client tools must be loaded on that computer (osql is only required for running the sample batch files on the local computer).</span></span>

-   <span data-ttu-id="d0c85-134">O SQL Server deve dar suporte à autenticação do Windows.</span><span class="sxs-lookup"><span data-stu-id="d0c85-134">The SQL Server must support Windows Authentication.</span></span>

-   <span data-ttu-id="d0c85-135">Verifique se a instância do SQL Server e o serviço do SQL Agent estão em execução.</span><span class="sxs-lookup"><span data-stu-id="d0c85-135">Ensure that the SQL Server Instance and SQL Agent Service are running.</span></span>

-   <span data-ttu-id="d0c85-136">Faça logon com uma conta de domínio que seja um administrador do SQL (sysadmin) no computador em que os scripts serão feitos.</span><span class="sxs-lookup"><span data-stu-id="d0c85-136">Log on with a domain account that is a SQL administrator (sysadmin) on the computer where the scripts will be done.</span></span>

<span data-ttu-id="d0c85-137">Os scripts são executados sob as credenciais de domínio do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="d0c85-137">The scripts runs under the logged-on user’s domain credentials.</span></span>

**<span data-ttu-id="d0c85-138">Criação de banco de dados usando scripts SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-138">Database Creation Using SQL Scripts</span></span>**

**<span data-ttu-id="d0c85-139">Tarefas a serem executadas pelos administradores do SQL:</span><span class="sxs-lookup"><span data-stu-id="d0c85-139">Tasks to be performed by SQL administrators:</span></span>**

1.  <span data-ttu-id="d0c85-140">Copie os scripts contidos na pasta support\\createdb da raiz do local de extração selecionado para o computador em que os scripts serão executados.</span><span class="sxs-lookup"><span data-stu-id="d0c85-140">Copy the scripts contained in the support\\createdb folder from the root of the selected extract location to the computer where the scripts will be run.</span></span> <span data-ttu-id="d0c85-141">Os arquivos a seguir são necessários para que os scripts sejam executados corretamente e devem ser chamados na ordem apresentada abaixo.</span><span class="sxs-lookup"><span data-stu-id="d0c85-141">The following files are required for the scripts to run properly and must be called in the order presented below.</span></span>

    -   <span data-ttu-id="d0c85-142">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-142">database.sql</span></span>

    -   <span data-ttu-id="d0c85-143">Roles. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-143">roles.sql</span></span>

    -   <span data-ttu-id="d0c85-144">tabela \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-144">table\_CODES.sql</span></span>

    -   <span data-ttu-id="d0c85-145">funções \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-145">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="d0c85-146">Tables. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-146">tables.sql</span></span>

    -   <span data-ttu-id="d0c85-147">functions. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-147">functions.sql</span></span>

    -   <span data-ttu-id="d0c85-148">views. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-148">views.sql</span></span>

    -   <span data-ttu-id="d0c85-149">procedimentos. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-149">procedures.sql</span></span>

    -   <span data-ttu-id="d0c85-150">triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-150">triggers.sql</span></span>

    -   <span data-ttu-id="d0c85-151">dados \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-151">data\_codes.sql</span></span>

    -   <span data-ttu-id="d0c85-152">dados \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-152">data\_messages.sql</span></span>

    -   <span data-ttu-id="d0c85-153">dados \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-153">data\_defaults.sql</span></span>

    -   <span data-ttu-id="d0c85-154">alertas \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-154">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="d0c85-155">DBVersion. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-155">dbversion.sql</span></span>

2.  <span data-ttu-id="d0c85-156">Revise e modifique, se necessário, o `database.sql` arquivo.</span><span class="sxs-lookup"><span data-stu-id="d0c85-156">Review and modify, if necessary, the `database.sql` file.</span></span> <span data-ttu-id="d0c85-157">As configurações padrão nomearão o banco de dados "APPVIRTDB".</span><span class="sxs-lookup"><span data-stu-id="d0c85-157">The default settings will name the database “APPVIRTDB.”</span></span>

    -   <span data-ttu-id="d0c85-158">Se necessário, substitua as instâncias de `APPVIRTDB` pelo `database name` que serão usadas.</span><span class="sxs-lookup"><span data-stu-id="d0c85-158">If necessary replace instances of `APPVIRTDB` with the `database name` that will be used.</span></span>

    -   <span data-ttu-id="d0c85-159">Modifique a `FILENAME` propriedade no script com o caminho apropriado para o SQL Server em que o banco de dados será criado.</span><span class="sxs-lookup"><span data-stu-id="d0c85-159">Modify the `FILENAME` property in the script with the appropriate path for the SQL Server where the database will be created.</span></span>

3.  <span data-ttu-id="d0c85-160">Revise e modifique, se necessário, o `database name [APPVIRTDB]` `roles.sql` arquivo no arquivo que foi usado no arquivo Database. Sql.</span><span class="sxs-lookup"><span data-stu-id="d0c85-160">Review and modify, if necessary, the `database name [APPVIRTDB]` in the `roles.sql` file that was used in the database.sql file.</span></span>

****

### <span data-ttu-id="d0c85-161">Exemplo de como automatizar o processo usando arquivos em lotes</span><span class="sxs-lookup"><span data-stu-id="d0c85-161">Example of how to automate the process using batch files</span></span>

<span data-ttu-id="d0c85-162">Se usado, os dois arquivos em lotes de exemplo fornecidos executam os scripts SQL da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d0c85-162">If used, the two sample batch files provided run the SQL scripts in the following manner:</span></span>

1.  **<span data-ttu-id="d0c85-163">Create\_schema.bat (1)</span><span class="sxs-lookup"><span data-stu-id="d0c85-163">Create\_schema.bat (1)</span></span>**

    -   <span data-ttu-id="d0c85-164">Database. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-164">database.sql</span></span>

    -   <span data-ttu-id="d0c85-165">Roles. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-165">roles.sql</span></span>

2.  **<span data-ttu-id="d0c85-166">Create\_tables.bat (2)</span><span class="sxs-lookup"><span data-stu-id="d0c85-166">Create\_tables.bat (2)</span></span>**

    -   <span data-ttu-id="d0c85-167">tabela \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-167">table\_CODES.sql</span></span>

    -   <span data-ttu-id="d0c85-168">funções \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-168">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="d0c85-169">Tables. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-169">tables.sql</span></span>

    -   <span data-ttu-id="d0c85-170">functions. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-170">functions.sql</span></span>

    -   <span data-ttu-id="d0c85-171">views. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-171">views.sql</span></span>

    -   <span data-ttu-id="d0c85-172">procedimentos. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-172">procedures.sql</span></span>

    -   <span data-ttu-id="d0c85-173">triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-173">triggers.sql</span></span>

    -   <span data-ttu-id="d0c85-174">dados \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-174">data\_codes.sql</span></span>

    -   <span data-ttu-id="d0c85-175">dados \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-175">data\_messages.sql</span></span>

    -   <span data-ttu-id="d0c85-176">dados \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-176">data\_defaults.sql</span></span>

    -   <span data-ttu-id="d0c85-177">alertas \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-177">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="d0c85-178">DBVersion. SQL</span><span class="sxs-lookup"><span data-stu-id="d0c85-178">dbversion.sql</span></span>

**<span data-ttu-id="d0c85-179">Observação</span><span class="sxs-lookup"><span data-stu-id="d0c85-179">Note</span></span>**  
<span data-ttu-id="d0c85-180">Uma consideração cuidadosa ao modificar os scripts deve ser feita e só deve ser feita por alguém com o conhecimento apropriado.</span><span class="sxs-lookup"><span data-stu-id="d0c85-180">Careful consideration when modifying the scripts must be taken and should only be done by someone with the appropriate knowledge.</span></span> <span data-ttu-id="d0c85-181">Além disso, dos arquivos de exemplo apresentados somente o seguinte deve ser alterado: **create\_schema.bat**, **create\_tables.bat**, **Database. SQL**e **Roles. SQL**.</span><span class="sxs-lookup"><span data-stu-id="d0c85-181">Also, of the sample files presented only the following should be changed: **create\_schema.bat**, **create\_tables.bat**, **database.sql**, and **roles.sql**.</span></span> <span data-ttu-id="d0c85-182">Todos os outros arquivos não devem ser modificados da mesma forma que isso pode fazer com que o banco de dados seja criado incorretamente, o que levará à falha dos serviços do App-V a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="d0c85-182">All other files should not be modified in any way as this could cause the database to be created incorrectly, which will lead to the failure of App-V services to be installed.</span></span>



<span data-ttu-id="d0c85-183">Os dois arquivos em lotes de exemplo devem ser colocados no mesmo diretório em que o restante dos scripts SQL foram copiados para o computador.</span><span class="sxs-lookup"><span data-stu-id="d0c85-183">The two sample batch files must be placed in the same directory where the rest of the SQL scripts were copied to on the computer.</span></span>

1.  <span data-ttu-id="d0c85-184">Execute o arquivo de exemplo **create\_schema.bat** para criar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d0c85-184">Run the sample **create\_schema.bat** file to create the database.</span></span> <span data-ttu-id="d0c85-185">Este script levará vários segundos para ser concluído e não deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="d0c85-185">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="d0c85-186">Execute o arquivo CREATE schema.bat do diretório em que foi copiado.</span><span class="sxs-lookup"><span data-stu-id="d0c85-186">Run the create schema.bat file from the directory where it was copied to.</span></span> <span data-ttu-id="d0c85-187">A sintaxe é: "Create\_schema.bat `SQLSERVERNAME` "</span><span class="sxs-lookup"><span data-stu-id="d0c85-187">Syntax is: “Create\_schema.bat `SQLSERVERNAME`”</span></span>

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   <span data-ttu-id="d0c85-189">Se esse script falhar durante a criação do novo banco de dados "APPVIRTDB", verifique o log indicado para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="d0c85-189">If this script fails during the creation of the new “APPVIRTDB” database, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="d0c85-190">Será necessário excluir o banco de dados que foi criado com uma execução parcial dos scripts para garantir que as tentativas subsequentes funcionem corretamente.</span><span class="sxs-lookup"><span data-stu-id="d0c85-190">It will be necessary to delete the database that was created with a partial running of the scripts in order to ensure that subsequent attempts will work properly.</span></span>

2.  <span data-ttu-id="d0c85-191">Execute o `create_tables.bat` arquivo para criar as tabelas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d0c85-191">Run the `create_tables.bat` file to create the tables in the database.</span></span> <span data-ttu-id="d0c85-192">Este script levará vários segundos para ser concluído e não deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="d0c85-192">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="d0c85-193">Execute o arquivo create\_tables.bat do diretório em que ele foi copiado.</span><span class="sxs-lookup"><span data-stu-id="d0c85-193">Run the create\_tables.bat file from the directory where it was copied.</span></span> <span data-ttu-id="d0c85-194">A sintaxe é: "create\_tables.bat `SQLSERVERNAME DBNAME` "</span><span class="sxs-lookup"><span data-stu-id="d0c85-194">Syntax is: “create\_tables.bat `SQLSERVERNAME DBNAME`”</span></span>

        ![create\-table.bat SQL do App-v 4,6](images/appv46sqlcreate-tablebat.gif)

        <span data-ttu-id="d0c85-196">Se o script falhar durante a criação das tabelas, verifique o log conforme indicado para corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="d0c85-196">If the script fails during the creation of the tables, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="d0c85-197">Será necessário excluir o banco de dados e executar o create\_schema.bat antes de tentar executar o arquivo create\_tables.bat em todas as tentativas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d0c85-197">It will be necessary to delete the database and run create\_schema.bat before attempting to run the create\_tables.bat file on all subsequent attempts.</span></span>

### <span data-ttu-id="d0c85-198">Definindo permissões no banco de dados do App-V</span><span class="sxs-lookup"><span data-stu-id="d0c85-198">Setting permissions on the App-V database</span></span>

<span data-ttu-id="d0c85-199">As contas a seguir precisarão ser criadas no SQL Server com permissões e funções específicas para o novo banco de dados para instalação, implantação e administração contínua do ambiente App-V.</span><span class="sxs-lookup"><span data-stu-id="d0c85-199">The following accounts will need to be created on the SQL server with specific permissions and roles to the new database for the installation, deployment and ongoing administration of the App-V environment.</span></span>

-   <span data-ttu-id="d0c85-200">Crie um login para o grupo App-V Administrators no SQL Server e o banco de dados APPVIRTDB para "domain\\App-V admins" (em que "domínio" e "App-V administradores" serão alterados para refletir seu próprio ambiente) e adicioná-los à função de banco de dados SFTAdmin e SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="d0c85-200">Create a login for the App-V administrators group on the SQL Server and the APPVIRTDB database for the “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment) and add them to the SFTAdmin and SFTEveryone database role.</span></span>

    ![App-v 4,6 o script SQL define permissões e funções](images/appv46sqlscriptsetpermsroles.gif)

-   <span data-ttu-id="d0c85-202">Conceda a este grupo a permissão "exibir qualquer definição" no nível global (isso permite que o processo de instalação do servidor de gerenciamento do Microsoft Application Virtualization Verifique se o logon do servidor de gerenciamento já existe).</span><span class="sxs-lookup"><span data-stu-id="d0c85-202">Grant this group “VIEW ANY DEFINITION” permission at the global level (This allows the Microsoft Application Virtualization Management Server setup process to verify that the Management Server login already exists).</span></span> <span data-ttu-id="d0c85-203">Em MS-SQL 2005 e acima restrições de acesso aos metadados contidos em Master. DB foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="d0c85-203">Under MS-SQL 2005 and above access restrictions to the metadata contained in master.db were added.</span></span> <span data-ttu-id="d0c85-204">O usuário criado na etapa anterior não terá, por padrão, os direitos necessários para a instalação do servidor.</span><span class="sxs-lookup"><span data-stu-id="d0c85-204">The user created in the previous step will by default not have the rights needed by the server installation.</span></span> <span data-ttu-id="d0c85-205">Abra as propriedades do logon criado anteriormente, propriedades de logon- &gt; protegívels.</span><span class="sxs-lookup"><span data-stu-id="d0c85-205">Open the properties of the previously created login, Login Properties-&gt;Securables.</span></span> <span data-ttu-id="d0c85-206">Adicione a instância de banco de dados e habilite "GRANT" para "View any Definition", conforme mostrado na captura de tela abaixo.</span><span class="sxs-lookup"><span data-stu-id="d0c85-206">Add the Database instance and enable “GRANT” for “View any definition” as shown in the screenshot below.</span></span>

    ![App-v 4,6 SQL script Grant Perm para View any def](images/appv46sqlscriptviewanydef.gif)

-   <span data-ttu-id="d0c85-208">Adicione uma função à tabela ROLE \ _ASSIGNMENTS para o logon criado na etapa anterior para permitir que os administradores do App-V acessem o console de gerenciamento do Application Virtualization, com a função = "administrador" e grupo \ _ref = "domain\\App-V administradores" (em que "domínio" e "App-V administradores" serão alterados para refletir seu próprio ambiente).</span><span class="sxs-lookup"><span data-stu-id="d0c85-208">Add a role to the ROLE\_ASSIGNMENTS table for the login created in the previous step to allow App-V administrators access to the Application Virtualization Management Console, with role = “ADMIN” and group\_ref = “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

    ![atribuição de função de script SQL do App-v 4,6](images/appv46sqlscriptroleassign.gif)

-   <span data-ttu-id="d0c85-210">Crie um login para o SQL Server e o banco de dados App-V para o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d0c85-210">Create login for SQL Server and App-V database for the Management Server.</span></span> <span data-ttu-id="d0c85-211">Essa conta é usada pelo servidor de gerenciamento do Microsoft Application Virtualization para se conectar ao repositório de dados e é responsável por atender solicitações de cliente para aplicativos em fluxo.</span><span class="sxs-lookup"><span data-stu-id="d0c85-211">This account is used by the Microsoft Application Virtualization Management Server to connect to the data store and is responsible for servicing client requests for streamed applications.</span></span> <span data-ttu-id="d0c85-212">Há duas opções, dependendo de onde o SQL Server e o servidor de gerenciamento devem ser instalados:</span><span class="sxs-lookup"><span data-stu-id="d0c85-212">There are two options, depending on where the SQL Server and Management Server are to be installed:</span></span>

    1.  <span data-ttu-id="d0c85-213">Se o servidor de gerenciamento e o SQL Server forem instalados no mesmo computador, adicione um login para o serviço NT AUTHORITY\\NETWORK e adicione-o às funções de banco de dados SFTUser e SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="d0c85-213">If Management Server and SQL Server are going to be installed on the same computer, add a login for NT AUTHORITY\\NETWORK SERVICE and add it to the SFTUser and SFTEveryone database roles.</span></span>

    2.  <span data-ttu-id="d0c85-214">Se o servidor de gerenciamento e o SQL Server forem instalados em computadores diferentes, adicione um login para "domain\\App-V Server Name $" (onde "App-V Server Name" é o nome do servidor em que o servidor de gerenciamento do App-V será instalado) e adicione-o às funções de banco de dados SFTUser e SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="d0c85-214">If the Management Server and SQL Server are to be installed on different computers, add a login for “domain\\App-V Server Name$” (where “App-V Server Name” is the name of the server where the App-V Management Server will be installed) and add it to the SFTUser and SFTEveryone database roles.</span></span>

-   <span data-ttu-id="d0c85-215">Abra a janela consulta na janela SQL e execute o seguinte SQL:</span><span class="sxs-lookup"><span data-stu-id="d0c85-215">Open the query window on the SQL window and run the following SQL:</span></span>

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    <span data-ttu-id="d0c85-216">Onde APPVIRTDB é o nome do banco de dados App-V criado no SQL Server na etapa anterior e o usuário que vai fazer a instalação do App-v Server precisa ser um membro de "domain\\App-V administradores" (em que "domínio" e "App-V administradores" será alterado para refletir seu próprio ambiente).</span><span class="sxs-lookup"><span data-stu-id="d0c85-216">Where the APPVIRTDB is the name of the App-V Database created on the SQL Server in the previous step, and the user who is going to do the install of the App-v server needs to be a member of “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

### <span data-ttu-id="d0c85-217">Tarefas a serem realizadas pelos administradores de infraestrutura</span><span class="sxs-lookup"><span data-stu-id="d0c85-217">Tasks to be performed by the Infrastructure administrators</span></span>

1.  <span data-ttu-id="d0c85-218">Administrador no grupo "App-V administradores" deve instalar o App-V.</span><span class="sxs-lookup"><span data-stu-id="d0c85-218">Administrator in the “App-V Admins” group should install App-V.</span></span>

    <span data-ttu-id="d0c85-219">Use as informações dos administradores do SQL para selecionar o SQL Server e o banco de dados criados nas etapas anteriores.</span><span class="sxs-lookup"><span data-stu-id="d0c85-219">Use information from the SQL administrators for selecting the SQL Server and database created in the previous steps.</span></span>

2.  <span data-ttu-id="d0c85-220">Administrador no grupo "App-V admins" conecta-se ao console de gerenciamento do Application Virtualization e exclui os seguintes objetos do console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d0c85-220">Administrator in the “App-V Admins” group logs in to Application Virtualization Management Console and deletes the following objects from the Management Console.</span></span>

    **<span data-ttu-id="d0c85-221">Aviso</span><span class="sxs-lookup"><span data-stu-id="d0c85-221">Warning</span></span>**  
    <span data-ttu-id="d0c85-222">Isso é necessário porque a configuração tradicional preenche determinados registros no banco de dados que não são preenchidos caso você execute a instalação em um banco de dados já existente.</span><span class="sxs-lookup"><span data-stu-id="d0c85-222">This is required as the traditional setup populates certain records in the database that are not populated if you run the install against an already existing database.</span></span> <span data-ttu-id="d0c85-223">Exclua os seguintes objetos:</span><span class="sxs-lookup"><span data-stu-id="d0c85-223">Delete the following objects:</span></span>

    -   <span data-ttu-id="d0c85-224">Em "grupos de servidores", "grupo padrão do servidor", excluir "servidor de gerenciamento do Application Virtualization"</span><span class="sxs-lookup"><span data-stu-id="d0c85-224">Under “Server Groups,” “Default Server Group,” delete “Application Virtualization Management Server”</span></span>

    -   <span data-ttu-id="d0c85-225">Em "grupos de servidores", "excluir" grupo padrão do servidor "</span><span class="sxs-lookup"><span data-stu-id="d0c85-225">Under “Server Groups,” delete “Default Server Group”</span></span>

    -   <span data-ttu-id="d0c85-226">Em "políticas de provedor", "excluir" provedor padrão "</span><span class="sxs-lookup"><span data-stu-id="d0c85-226">Under “Provider Policies,” delete “Default Provider”</span></span>



3.  <span data-ttu-id="d0c85-227">Administrador no grupo App-V admins deve criar:</span><span class="sxs-lookup"><span data-stu-id="d0c85-227">Administrator in the App-V admins group should then create:</span></span>

    -   <span data-ttu-id="d0c85-228">Em "políticas de provedor", crie uma nova política de provedor</span><span class="sxs-lookup"><span data-stu-id="d0c85-228">Under “Provider Policies,” create a New Provider Policy</span></span>

    -   <span data-ttu-id="d0c85-229">Criar um "grupo de servidor padrão"</span><span class="sxs-lookup"><span data-stu-id="d0c85-229">Create a “Default Server Group”</span></span>

        **<span data-ttu-id="d0c85-230">Observação</span><span class="sxs-lookup"><span data-stu-id="d0c85-230">Note</span></span>**  
        <span data-ttu-id="d0c85-231">Você deve criar um grupo de "servidor padrão" mesmo se não for usado.</span><span class="sxs-lookup"><span data-stu-id="d0c85-231">You must create a “Default Server” group even if you will not be used.</span></span> <span data-ttu-id="d0c85-232">O instalador do servidor só procura o "grupo padrão do servidor" ao tentar adicionar o servidor.</span><span class="sxs-lookup"><span data-stu-id="d0c85-232">The server installer only looks for the "Default Server Group" when trying to add the server.</span></span>  <span data-ttu-id="d0c85-233">Se não houver um "grupo de servidores padrão", a instalação não será bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d0c85-233">If there is no "Default Server Group" then the installation will fail.</span></span> <span data-ttu-id="d0c85-234">Se você planeja usar grupos do servidor diferentes do padrão, é preciso manter o "grupo padrão do servidor" se planejar adicionar servidores de gerenciamento do App-V subsequentes à sua infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="d0c85-234">If you plan on using server groups other than the default that is fine, it’s just necessary to retain the "Default Server Group" if you plan on adding subsequent App-V Management Servers to your infrastructure.</span></span>



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <span data-ttu-id="d0c85-235">Conclusão</span><span class="sxs-lookup"><span data-stu-id="d0c85-235">Conclusion</span></span>


<span data-ttu-id="d0c85-236">Em conclusão, as informações neste documento permitem que um administrador trabalhe com os administradores do SQL para desenvolver um caminho de implantação que funcione para as divisões administrativas e de segurança de uma organização.</span><span class="sxs-lookup"><span data-stu-id="d0c85-236">In conclusion, the information in this document allows an administrator to work with the SQL administrators to develop a deployment path that works for the security and administrative divisions in an organization.</span></span> <span data-ttu-id="d0c85-237">Depois de ler este documento e testar as tarefas documentadas, um administrador deve estar pronto para implementar sua infraestrutura do App-V nesse tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="d0c85-237">After reading this document and testing the tasks documented, an administrator should be ready to implement their App-V infrastructure in this type of environment.</span></span>









