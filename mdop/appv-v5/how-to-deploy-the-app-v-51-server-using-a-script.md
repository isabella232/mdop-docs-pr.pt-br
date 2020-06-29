---
title: Como implantar o servidor App-V 5.1 usando um script
description: Como implantar o servidor App-V 5.1 usando um script
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10796422"
---
# <span data-ttu-id="ef892-103">Como implantar o servidor App-V 5.1 usando um script</span><span class="sxs-lookup"><span data-stu-id="ef892-103">How to Deploy the App-V 5.1 Server Using a Script</span></span>

<span data-ttu-id="ef892-104">Para concluir a configuração do servidor do **appv\_server\_setup.exe** com êxito usando a linha de comando, você deve especificar e combinar vários parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ef892-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

## <span data-ttu-id="ef892-105">Instalar o servidor do App-V 5,1 usando um script</span><span class="sxs-lookup"><span data-stu-id="ef892-105">Install the App-V 5.1 server using a script</span></span>

- <span data-ttu-id="ef892-106">Use as informações a seguir sobre como instalar o servidor do App-V 5,1 usando a linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ef892-106">Use the following information about installing the App-V 5.1 server using the command line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef892-107">As informações nas tabelas a seguir também podem ser acessadas usando a linha de comando digitando o seguinte comando: **appv\_server\_setup.exe/?**.</span><span class="sxs-lookup"><span data-stu-id="ef892-107">The information in the following tables can also be accessed using the command line by typing the following command: **appv\_server\_setup.exe /?**.</span></span>

### <span data-ttu-id="ef892-108">Instalar o servidor de gerenciamento e o banco de dados de gerenciamento em um computador local</span><span class="sxs-lookup"><span data-stu-id="ef892-108">Install the Management server and Management database on a local machine</span></span>

<span data-ttu-id="ef892-109">Os parâmetros a seguir são válidos com as instâncias padrão e personalizadas do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ef892-109">The following parameters are valid with both the default and custom instance of Microsoft SQL Server:</span></span>

- <span data-ttu-id="ef892-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-110">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ef892-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-111">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ef892-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-112">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-113">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ef892-114">/DB_PREDEPLOY_MANAGEMENT</span></span>
- <span data-ttu-id="ef892-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="ef892-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-116">/MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="ef892-117">Exemplo: usando uma instância personalizada do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef892-117">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### <span data-ttu-id="ef892-118">Instalar o servidor de gerenciamento usando um banco de dados de gerenciamento existente em um computador local</span><span class="sxs-lookup"><span data-stu-id="ef892-118">Install the Management server using an existing Management database on a local machine</span></span>

<span data-ttu-id="ef892-119">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-119">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-120">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-120">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ef892-121">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-121">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ef892-122">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-122">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-123">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-123">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="ef892-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ef892-126">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-126">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="ef892-127">Para usar uma instância personalizada do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-127">To use a custom instance of Microsoft SQL Server, use the following parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-128">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-128">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ef892-129">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-129">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ef892-130">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-130">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-131">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-131">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="ef892-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ef892-134">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-134">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="ef892-135">Exemplo: usando uma instância personalizada do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef892-135">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="ef892-136">Instalar o servidor de gerenciamento usando um banco de dados de gerenciamento existente em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="ef892-136">Install the Management server using an existing Management database on a remote machine</span></span>

<span data-ttu-id="ef892-137">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-137">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-138">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-138">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ef892-139">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-139">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ef892-140">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-140">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-141">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-141">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="ef892-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ef892-144">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-144">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="ef892-145">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-145">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-146">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-146">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="ef892-147">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-147">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="ef892-148">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-148">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-149">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-149">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="ef892-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ef892-152">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-152">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="ef892-153">Exemplo: usando uma instância personalizada do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ef892-153">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="ef892-154">Instalar o banco de dados de gerenciamento e o servidor de gerenciamento no mesmo computador</span><span class="sxs-lookup"><span data-stu-id="ef892-154">Install the Management database and the Management Server on the same computer</span></span>

<span data-ttu-id="ef892-155">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-155">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-156">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ef892-156">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="ef892-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ef892-158">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-158">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="ef892-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="ef892-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="ef892-161">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-161">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-162">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ef892-162">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="ef892-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ef892-164">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-164">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="ef892-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="ef892-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="ef892-167">Exemplo: usando uma instância personalizada do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef892-167">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="ef892-168">Instalar o banco de dados de gerenciamento em um computador diferente do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ef892-168">Install the Management database on a different computer than the Management server</span></span>

<span data-ttu-id="ef892-169">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-169">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-170">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ef892-170">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="ef892-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ef892-172">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-172">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="ef892-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="ef892-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="ef892-175">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-175">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-176">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ef892-176">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="ef892-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ef892-178">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-178">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="ef892-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="ef892-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="ef892-181">Exemplo: usando uma instância personalizada do Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef892-181">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="ef892-182">Instalar o Publishing Server</span><span class="sxs-lookup"><span data-stu-id="ef892-182">Install the publishing server</span></span>

<span data-ttu-id="ef892-183">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ef892-183">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span>

- <span data-ttu-id="ef892-184">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-184">/PUBLISHING_SERVER</span></span>
- <span data-ttu-id="ef892-185">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-185">/PUBLISHING_MGT_SERVER</span></span>
- <span data-ttu-id="ef892-186">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-186">/PUBLISHING_WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-187">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-187">/PUBLISHING_WEBSITE_PORT</span></span>

**<span data-ttu-id="ef892-188">Exemplo: usando uma instância personalizada do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ef892-188">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### <span data-ttu-id="ef892-189">Instalar o servidor de relatórios e o banco de dados de relatórios em um computador local</span><span class="sxs-lookup"><span data-stu-id="ef892-189">Install the Reporting server and Reporting database on a local machine</span></span>

<span data-ttu-id="ef892-190">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-190">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-191">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-191">/REPORTING _SERVER</span></span>
- <span data-ttu-id="ef892-192">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-192">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-193">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-193">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-194">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ef892-194">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="ef892-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ef892-196">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-196">/REPORTING _DB_NAME</span></span>

<span data-ttu-id="ef892-197">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-197">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-198">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-198">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="ef892-199">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-199">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="ef892-200">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-200">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-201">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-201">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-202">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ef892-202">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="ef892-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ef892-204">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-204">/REPORTING _DB_NAME</span></span>

**<span data-ttu-id="ef892-205">Exemplo: usando uma instância personalizada do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ef892-205">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="ef892-206">Instalar o servidor de relatórios e usar um banco de dados de relatórios existente em um computador local</span><span class="sxs-lookup"><span data-stu-id="ef892-206">Install the Reporting server and using an existing Reporting database on a local machine</span></span>

<span data-ttu-id="ef892-207">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-207">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-208">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-208">/REPORTING _SERVER</span></span>
- <span data-ttu-id="ef892-209">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-209">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-210">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-210">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="ef892-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ef892-213">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-213">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="ef892-214">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-214">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-215">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-215">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="ef892-216">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-216">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="ef892-217">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-217">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-218">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-218">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="ef892-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ef892-221">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-221">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="ef892-222">Exemplo: usando uma instância personalizada do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ef892-222">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="ef892-223">Instalar o servidor de relatórios usando um banco de dados de relatórios existente em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="ef892-223">Install the Reporting server using an existing Reporting database on a remote machine</span></span>

<span data-ttu-id="ef892-224">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-224">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-225">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-225">/REPORTING _SERVER</span></span>
- <span data-ttu-id="ef892-226">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-226">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-227">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-227">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="ef892-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ef892-230">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-230">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="ef892-231">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-231">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-232">/REPORTING _SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-232">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="ef892-233">/REPORTING _ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-233">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="ef892-234">/REPORTING _WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-234">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="ef892-235">/REPORTING _WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-235">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="ef892-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="ef892-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ef892-238">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-238">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="ef892-239">Exemplo: usando uma instância personalizada do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ef892-239">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="ef892-240">Instalar o banco de dados de relatórios no mesmo computador que o servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="ef892-240">Install the Reporting database on the same computer as the Reporting server</span></span>

<span data-ttu-id="ef892-241">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-241">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-242">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ef892-242">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="ef892-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="ef892-244">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-244">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="ef892-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="ef892-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="ef892-247">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-247">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-248">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ef892-248">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="ef892-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="ef892-250">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-250">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="ef892-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="ef892-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="ef892-253">Exemplo: usando uma instância personalizada do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ef892-253">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="ef892-254">Instalar o banco de dados de relatórios em um computador diferente do que o servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="ef892-254">Install the Reporting database on a different computer than the Reporting server</span></span>

<span data-ttu-id="ef892-255">Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-255">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="ef892-256">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ef892-256">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="ef892-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="ef892-258">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-258">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="ef892-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="ef892-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="ef892-261">Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):</span><span class="sxs-lookup"><span data-stu-id="ef892-261">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="ef892-262">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ef892-262">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="ef892-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>
- <span data-ttu-id="ef892-264">/REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-264">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="ef892-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="ef892-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="ef892-267">Exemplo: usando uma instância personalizada do Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="ef892-267">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="ef892-268">Definições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-268">Parameter Definitions</span></span>

#### <span data-ttu-id="ef892-269">Parâmetros gerais</span><span class="sxs-lookup"><span data-stu-id="ef892-269">General Parameters</span></span>

| <span data-ttu-id="ef892-270">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-270">Parameter</span></span> | <span data-ttu-id="ef892-271">Informações</span><span class="sxs-lookup"><span data-stu-id="ef892-271">Information</span></span> |
|--|--|
| <span data-ttu-id="ef892-272">/QUIET</span><span class="sxs-lookup"><span data-stu-id="ef892-272">/QUIET</span></span> | <span data-ttu-id="ef892-273">Especifica a instalação silenciosa.</span><span class="sxs-lookup"><span data-stu-id="ef892-273">Specifies silent install.</span></span> |
| <span data-ttu-id="ef892-274">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="ef892-274">/UNINSTALL</span></span> | <span data-ttu-id="ef892-275">Especifica uma desinstalação.</span><span class="sxs-lookup"><span data-stu-id="ef892-275">Specifies an uninstall.</span></span> |
| <span data-ttu-id="ef892-276">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="ef892-276">/LAYOUT</span></span> | <span data-ttu-id="ef892-277">Especifica a ação de layout.</span><span class="sxs-lookup"><span data-stu-id="ef892-277">Specifies layout action.</span></span> <span data-ttu-id="ef892-278">Isso extrai os arquivos MSIs e script para uma pasta sem realmente instalar o produto.</span><span class="sxs-lookup"><span data-stu-id="ef892-278">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="ef892-279">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-279">No value is expected.</span></span> |
| <span data-ttu-id="ef892-280">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="ef892-280">/LAYOUTDIR</span></span> | <span data-ttu-id="ef892-281">Especifica o diretório de layout.</span><span class="sxs-lookup"><span data-stu-id="ef892-281">Specifies the layout directory.</span></span> <span data-ttu-id="ef892-282">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-282">Takes a string.</span></span> <span data-ttu-id="ef892-283">Exemplo de uso: **/LAYOUTDIR = "servidor de virtualização C:\\Application"**</span><span class="sxs-lookup"><span data-stu-id="ef892-283">Example usage: **/LAYOUTDIR="C:\\Application Virtualization Server"**</span></span> |
| <span data-ttu-id="ef892-284">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="ef892-284">/INSTALLDIR</span></span> | <span data-ttu-id="ef892-285">Especifica o diretório de instalação.</span><span class="sxs-lookup"><span data-stu-id="ef892-285">Specifies the installation directory.</span></span> <span data-ttu-id="ef892-286">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-286">Takes a string.</span></span> <span data-ttu-id="ef892-287">Exemplo de uso: **/installdir = "C:\\Arquivos Files\\Application Virtualization\\Server"**</span><span class="sxs-lookup"><span data-stu-id="ef892-287">Example usage: **/INSTALLDIR="C:\\Program Files\\Application Virtualization\\Server"**</span></span> |
| <span data-ttu-id="ef892-288">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="ef892-288">/MUOPTIN</span></span> | <span data-ttu-id="ef892-289">Habilita o Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="ef892-289">Enables Microsoft Update.</span></span> <span data-ttu-id="ef892-290">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-290">No value is expected.</span></span> |
| <span data-ttu-id="ef892-291">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="ef892-291">/ACCEPTEULA</span></span> | <span data-ttu-id="ef892-292">Aceita o contrato de licença.</span><span class="sxs-lookup"><span data-stu-id="ef892-292">Accepts the license agreement.</span></span> <span data-ttu-id="ef892-293">Isso é necessário para uma instalação automática.</span><span class="sxs-lookup"><span data-stu-id="ef892-293">This is required for an unattended installation.</span></span> <span data-ttu-id="ef892-294">Exemplo de uso: **/AcceptEula** ou **/ACCEPTEULA = 1**</span><span class="sxs-lookup"><span data-stu-id="ef892-294">Example usage: **/ACCEPTEULA** or **/ACCEPTEULA=1**</span></span> |

#### <span data-ttu-id="ef892-295">Parâmetros de instalação do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ef892-295">Management Server Installation Parameters</span></span>

|<span data-ttu-id="ef892-296">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-296">Parameter</span></span> |<span data-ttu-id="ef892-297">Informações</span><span class="sxs-lookup"><span data-stu-id="ef892-297">Information</span></span> |
|--|--|
| <span data-ttu-id="ef892-298">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-298">/MANAGEMENT_SERVER</span></span> | <span data-ttu-id="ef892-299">Especifica que o servidor de gerenciamento será instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-299">Specifies that the management server will be installed.</span></span> <span data-ttu-id="ef892-300">Nenhum valor é esperado</span><span class="sxs-lookup"><span data-stu-id="ef892-300">No value is expected</span></span> |
| <span data-ttu-id="ef892-301">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-301">/MANAGEMENT_ADMINACCOUNT</span></span> | <span data-ttu-id="ef892-302">Especifica a conta à qual o acesso de administrador será permitido para o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ef892-302">Specifies the account that will be allowed Administrator access to the management server.</span></span> <span data-ttu-id="ef892-303">Pode ser uma conta de usuário ou um grupo.</span><span class="sxs-lookup"><span data-stu-id="ef892-303">This can be a user account or a group.</span></span> <span data-ttu-id="ef892-304">Exemplo de uso: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**.</span><span class="sxs-lookup"><span data-stu-id="ef892-304">Example usage: **/MANAGEMENT_ADMINACCOUNT="mydomain\\admin"**.</span></span> <span data-ttu-id="ef892-305">Se **/MANAGEMENT_SERVER** não for especificado, isso será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef892-305">If **/MANAGEMENT_SERVER** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="ef892-306">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-306">/MANAGEMENT_WEBSITE_NAME</span></span> | <span data-ttu-id="ef892-307">Especifica o nome do site que será criado para o serviço de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ef892-307">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="ef892-308">Exemplo de uso: **/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft App-V"**</span><span class="sxs-lookup"><span data-stu-id="ef892-308">Example usage: **/MANAGEMENT_WEBSITE_NAME="Microsoft App-V Management Service"**</span></span> |
| <span data-ttu-id="ef892-309">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-309">MANAGEMENT_WEBSITE_PORT</span></span> | <span data-ttu-id="ef892-310">Especifica o número da porta que será usada pelo serviço de gerenciamento que será usado.</span><span class="sxs-lookup"><span data-stu-id="ef892-310">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="ef892-311">Exemplo de uso: **/MANAGEMENT_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="ef892-311">Example usage: **/MANAGEMENT_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="ef892-312">Parâmetros para o banco de dados do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ef892-312">Parameters for the Management Server Database</span></span>

| <span data-ttu-id="ef892-313">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-313">Parameter</span></span> | <span data-ttu-id="ef892-314">Informações</span><span class="sxs-lookup"><span data-stu-id="ef892-314">Information</span></span> |
|--|--|
| <span data-ttu-id="ef892-315">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="ef892-315">/DB_PREDEPLOY_MANAGEMENT</span></span> | <span data-ttu-id="ef892-316">Especifica que o banco de dados de gerenciamento será instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-316">Specifies that the management database will be installed.</span></span> <span data-ttu-id="ef892-317">Você deve ter permissões de banco de dados suficientes para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="ef892-317">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="ef892-318">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-318">No value is expected.</span></span> |
| <span data-ttu-id="ef892-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="ef892-320">Indica que a instância SQL padrão deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="ef892-320">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="ef892-321">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-321">No value is expected.</span></span> |
| <span data-ttu-id="ef892-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="ef892-323">Especifica o nome da instância SQL personalizada que deve ser usada para criar um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ef892-323">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="ef892-324">Exemplo de uso: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"**.</span><span class="sxs-lookup"><span data-stu-id="ef892-324">Example usage: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**.</span></span> <span data-ttu-id="ef892-325">Se **/DB_PREDEPLOY_MANAGEMENT** não for especificado, isso será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef892-325">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="ef892-326">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-326">/MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="ef892-327">Especifica o nome do novo banco de dados de gerenciamento que deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="ef892-327">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="ef892-328">Exemplo de uso: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="ef892-328">Example usage: **/MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="ef892-329">Se **/DB_PREDEPLOY_MANAGEMENT** não for especificado, isso será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef892-329">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="ef892-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="ef892-331">Indica se o servidor de gerenciamento que vai acessar o banco de dados está instalado no servidor local.</span><span class="sxs-lookup"><span data-stu-id="ef892-331">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="ef892-332">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-332">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="ef892-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="ef892-334">Especifica a conta de máquina do computador remoto em que o servidor de gerenciamento será instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-334">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="ef892-335">Exemplo de uso: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"**</span><span class="sxs-lookup"><span data-stu-id="ef892-335">Example usage: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="domain\\computername"**</span></span> |
| <span data-ttu-id="ef892-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="ef892-337">Indica a conta de administrador que será usada para instalar o servidor de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ef892-337">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="ef892-338">Exemplo de uso: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="ef892-338">Example usage: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT ="domain\\alias"**</span></span> |

#### <span data-ttu-id="ef892-339">Parâmetros para instalar o Publishing Server</span><span class="sxs-lookup"><span data-stu-id="ef892-339">Parameters for Installing Publishing Server</span></span>

| <span data-ttu-id="ef892-340">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-340">Parameter</span></span> | <span data-ttu-id="ef892-341">Informações</span><span class="sxs-lookup"><span data-stu-id="ef892-341">Information</span></span> |
|--|--|
| <span data-ttu-id="ef892-342">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-342">/PUBLISHING_SERVER</span></span> | <span data-ttu-id="ef892-343">Especifica que o servidor de publicação será instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-343">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="ef892-344">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-344">No value is expected.</span></span> |
| <span data-ttu-id="ef892-345">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-345">/PUBLISHING_MGT_SERVER</span></span> | <span data-ttu-id="ef892-346">Especifica a URL para o serviço de gerenciamento ao qual o servidor de publicação será conectado.</span><span class="sxs-lookup"><span data-stu-id="ef892-346">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="ef892-347">Exemplo de uso: **http:// &lt; Management Server Name &gt; : número &lt; &gt; de porta do servidor de gerenciamento**.</span><span class="sxs-lookup"><span data-stu-id="ef892-347">Example usage: **http://&lt;management server name&gt;:&lt;Management server port number&gt;**.</span></span> <span data-ttu-id="ef892-348">Se **/PUBLISHING_SERVER** não for usado, este parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef892-348">If **/PUBLISHING_SERVER** is not used, this parameter will be ignored.</span></span> |
| <span data-ttu-id="ef892-349">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-349">/PUBLISHING_WEBSITE_NAME</span></span> | <span data-ttu-id="ef892-350">Especifica o nome do site que será criado para o serviço de publicação.</span><span class="sxs-lookup"><span data-stu-id="ef892-350">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="ef892-351">Exemplo de uso: **/PUBLISHING_WEBSITE_NAME = "serviço Microsoft App-V Publishing"**</span><span class="sxs-lookup"><span data-stu-id="ef892-351">Example usage: **/PUBLISHING_WEBSITE_NAME="Microsoft App-V Publishing Service"**</span></span> |
| <span data-ttu-id="ef892-352">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-352">/PUBLISHING_WEBSITE_PORT</span></span> | <span data-ttu-id="ef892-353">Especifica o número da porta usada pelo serviço de publicação.</span><span class="sxs-lookup"><span data-stu-id="ef892-353">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="ef892-354">Exemplo de uso: **/PUBLISHING_WEBSITE_PORT = 83**</span><span class="sxs-lookup"><span data-stu-id="ef892-354">Example usage: **/PUBLISHING_WEBSITE_PORT=83**</span></span> |

#### <span data-ttu-id="ef892-355">Parâmetros do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="ef892-355">Parameters for Reporting Server</span></span>

| <span data-ttu-id="ef892-356">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-356">Parameter</span></span> | <span data-ttu-id="ef892-357">Informações</span><span class="sxs-lookup"><span data-stu-id="ef892-357">Information</span></span> |
|--|--|
| <span data-ttu-id="ef892-358">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="ef892-358">/REPORTING_SERVER</span></span> | <span data-ttu-id="ef892-359">Especifica que o servidor de relatórios será instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-359">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="ef892-360">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-360">No value is expected.</span></span> |
| <span data-ttu-id="ef892-361">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-361">/REPORTING_WEBSITE_NAME</span></span> | <span data-ttu-id="ef892-362">Especifica o nome do site que será criado para o serviço de relatório.</span><span class="sxs-lookup"><span data-stu-id="ef892-362">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="ef892-363">Exemplo de uso: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"**</span><span class="sxs-lookup"><span data-stu-id="ef892-363">Example usage: **/REPORTING_WEBSITE_NAME="Microsoft App-V ReportingService"**</span></span> |
| <span data-ttu-id="ef892-364">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="ef892-364">/REPORTING_WEBSITE_PORT</span></span> | <span data-ttu-id="ef892-365">Especifica o número da porta que o serviço de relatórios vai usar.</span><span class="sxs-lookup"><span data-stu-id="ef892-365">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="ef892-366">Exemplo de uso: **/REPORTING_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="ef892-366">Example usage: **/REPORTING_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="ef892-367">Parâmetros para usar um banco de dados do servidor de relatórios existente</span><span class="sxs-lookup"><span data-stu-id="ef892-367">Parameters for using an Existing Reporting Server Database</span></span>

| <span data-ttu-id="ef892-368">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-368">Parameter</span></span> | <span data-ttu-id="ef892-369">Informações</span><span class="sxs-lookup"><span data-stu-id="ef892-369">Information</span></span> |
|--|--|
| <span data-ttu-id="ef892-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="ef892-371">Indica que o Microsoft SQL Server está instalado no servidor local.</span><span class="sxs-lookup"><span data-stu-id="ef892-371">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="ef892-372">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-372">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="ef892-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="ef892-374">Especifica o nome do computador remoto no qual o SQL Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-374">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="ef892-375">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-375">Takes a string.</span></span> <span data-ttu-id="ef892-376">Exemplo de uso: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="ef892-376">Example usage: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="ef892-377">/EXISTING_ _DB_SQLINSTANCE_USE_DEFAULT DE RELATÓRIO</span><span class="sxs-lookup"><span data-stu-id="ef892-377">/EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="ef892-378">Indica que a instância SQL padrão deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="ef892-378">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="ef892-379">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-379">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="ef892-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="ef892-381">Especifica o nome da instância SQL personalizada que deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="ef892-381">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="ef892-382">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-382">Takes a string.</span></span> <span data-ttu-id="ef892-383">Exemplo de uso: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"**</span><span class="sxs-lookup"><span data-stu-id="ef892-383">Example usage: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="ef892-384">/EXISTING_ _DB_NAME DE RELATÓRIO</span><span class="sxs-lookup"><span data-stu-id="ef892-384">/EXISTING_ REPORTING _DB_NAME</span></span> | <span data-ttu-id="ef892-385">Especifica o nome do banco de dados de relatórios existente que deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="ef892-385">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="ef892-386">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-386">Takes a string.</span></span> <span data-ttu-id="ef892-387">Exemplo de uso: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"**</span><span class="sxs-lookup"><span data-stu-id="ef892-387">Example usage: **/EXISTING_REPORTING_DB_NAME="AppVReporting"**</span></span> |

#### <span data-ttu-id="ef892-388">Parâmetros para instalar o banco de dados do servidor de relatório</span><span class="sxs-lookup"><span data-stu-id="ef892-388">Parameters for installing Reporting Server Database</span></span>

| <span data-ttu-id="ef892-389">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-389">Parameter</span></span> | <span data-ttu-id="ef892-390">Informações</span><span class="sxs-lookup"><span data-stu-id="ef892-390">Information</span></span> |
|--|--|
| <span data-ttu-id="ef892-391">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="ef892-391">/DB_PREDEPLOY_REPORTING</span></span> | <span data-ttu-id="ef892-392">Especifica que o banco de dados de relatórios será instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-392">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="ef892-393">As permissões do DBA são necessárias para esta instalação.</span><span class="sxs-lookup"><span data-stu-id="ef892-393">DBA permissions are required for this installation.</span></span> <span data-ttu-id="ef892-394">Nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-394">No value is expected.</span></span> |
| <span data-ttu-id="ef892-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="ef892-396">Especifica o nome da instância SQL personalizada que deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="ef892-396">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="ef892-397">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-397">Takes a string.</span></span> <span data-ttu-id="ef892-398">Exemplo de uso: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"**</span><span class="sxs-lookup"><span data-stu-id="ef892-398">Example usage: **/REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="ef892-399">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-399">/REPORTING_DB_NAME</span></span> | <span data-ttu-id="ef892-400">Especifica o nome do novo banco de dados de relatórios que deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="ef892-400">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="ef892-401">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-401">Takes a string.</span></span> <span data-ttu-id="ef892-402">Exemplo de uso: **/REPORTING_DB_NAME = "AppVMgmtDB"**</span><span class="sxs-lookup"><span data-stu-id="ef892-402">Example usage: **/REPORTING_DB_NAME="AppVMgmtDB"**</span></span> |
| <span data-ttu-id="ef892-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="ef892-404">Indica que o servidor de relatórios que vai acessar o banco de dados está instalado no servidor local.</span><span class="sxs-lookup"><span data-stu-id="ef892-404">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="ef892-405">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-405">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="ef892-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="ef892-407">Especifica a conta de máquina do computador remoto em que o servidor de relatórios será instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-407">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="ef892-408">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-408">Takes a string.</span></span> <span data-ttu-id="ef892-409">Exemplo de uso: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"**</span><span class="sxs-lookup"><span data-stu-id="ef892-409">Example usage: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="domain\computername"**</span></span> |
| <span data-ttu-id="ef892-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="ef892-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="ef892-411">Indica a conta de administrador que será usada para instalar o servidor de relatórios do App-V.</span><span class="sxs-lookup"><span data-stu-id="ef892-411">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="ef892-412">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-412">Takes a string.</span></span> <span data-ttu-id="ef892-413">Exemplo de uso: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="ef892-413">Example usage: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="domain\\alias"**</span></span> |

#### <span data-ttu-id="ef892-414">Parâmetros para usar um banco de dados existente do servidor de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ef892-414">Parameters for using an existing Management Server Database</span></span>

| <span data-ttu-id="ef892-415">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef892-415">Parameter</span></span> | <span data-ttu-id="ef892-416">Informações</span><span class="sxs-lookup"><span data-stu-id="ef892-416">Information</span></span> |
|--|--|
| <span data-ttu-id="ef892-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="ef892-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="ef892-418">Indica que o SQL Server está instalado no servidor local.</span><span class="sxs-lookup"><span data-stu-id="ef892-418">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="ef892-419">Parâmetro de opção; portanto, nenhum valor é esperado. Se **/DB_PREDEPLOY_MANAGEMENT** for especificado, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef892-419">Switch parameter so no value is expected.If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="ef892-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="ef892-421">Especifica o nome do computador remoto no qual o SQL Server está instalado.</span><span class="sxs-lookup"><span data-stu-id="ef892-421">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="ef892-422">Usa uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef892-422">Takes a string.</span></span> <span data-ttu-id="ef892-423">Exemplo de uso: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="ef892-423">Example usage: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="ef892-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef892-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="ef892-425">Indica que a instância SQL padrão deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="ef892-425">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="ef892-426">Parâmetro de opção; portanto, nenhum valor é esperado.</span><span class="sxs-lookup"><span data-stu-id="ef892-426">Switch parameter so no value is expected.</span></span> <span data-ttu-id="ef892-427">Se **/DB_PREDEPLOY_MANAGEMENT** for especificado, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef892-427">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="ef892-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef892-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="ef892-429">Especifica o nome da instância SQL personalizada que será usada.</span><span class="sxs-lookup"><span data-stu-id="ef892-429">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="ef892-430">Exemplo de uso **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**.</span><span class="sxs-lookup"><span data-stu-id="ef892-430">Example usage **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="AppVManagement"**.</span></span> <span data-ttu-id="ef892-431">Se **/DB_PREDEPLOY_MANAGEMENT** for especificado, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef892-431">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="ef892-432">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="ef892-432">/EXISTING_MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="ef892-433">Especifica o nome do banco de dados de gerenciamento existente que deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="ef892-433">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="ef892-434">Exemplo de uso: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="ef892-434">Example usage: **/EXISTING_MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="ef892-435">Se **/DB_PREDEPLOY_MANAGEMENT** for especificado, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ef892-435">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |

<span data-ttu-id="ef892-436">Tem um problema com o App-V?</span><span class="sxs-lookup"><span data-stu-id="ef892-436">Got an App-V issue?</span></span> <span data-ttu-id="ef892-437">Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ef892-437">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ef892-438">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef892-438">Related topics</span></span>

[<span data-ttu-id="ef892-439">Implantação do servidor App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ef892-439">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)
