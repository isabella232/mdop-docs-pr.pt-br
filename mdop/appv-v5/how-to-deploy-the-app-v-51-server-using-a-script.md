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
# Como implantar o servidor App-V 5.1 usando um script

Para concluir a configuração do servidor do **appv\_server\_setup.exe** com êxito usando a linha de comando, você deve especificar e combinar vários parâmetros.

## Instalar o servidor do App-V 5,1 usando um script

- Use as informações a seguir sobre como instalar o servidor do App-V 5,1 usando a linha de comando.

    > [!NOTE]
    > As informações nas tabelas a seguir também podem ser acessadas usando a linha de comando digitando o seguinte comando: **appv\_server\_setup.exe/?**.

### Instalar o servidor de gerenciamento e o banco de dados de gerenciamento em um computador local

Os parâmetros a seguir são válidos com as instâncias padrão e personalizadas do Microsoft SQL Server:

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /DB_PREDEPLOY_MANAGEMENT
- /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT
- /MANAGEMENT_DB_NAME

**Exemplo: usando uma instância personalizada do Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### Instalar o servidor de gerenciamento usando um banco de dados de gerenciamento existente em um computador local

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Para usar uma instância personalizada do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância padrão em *itálico*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Exemplo: usando uma instância personalizada do Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Instalar o servidor de gerenciamento usando um banco de dados de gerenciamento existente em um computador remoto

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Exemplo: usando uma instância personalizada do Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Instalar o banco de dados de gerenciamento e o servidor de gerenciamento no mesmo computador

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Exemplo: usando uma instância personalizada do Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Instalar o banco de dados de gerenciamento em um computador diferente do servidor de gerenciamento

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Exemplo: usando uma instância personalizada do Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Instalar o Publishing Server

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros:

- /PUBLISHING_SERVER
- /PUBLISHING_MGT_SERVER
- /PUBLISHING_WEBSITE_NAME
- /PUBLISHING_WEBSITE_PORT

**Exemplo: usando uma instância personalizada do Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### Instalar o servidor de relatórios e o banco de dados de relatórios em um computador local

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /REPORTING _DB_NAME

Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_CUSTOM_SQLINSTANCE*
- /REPORTING _DB_NAME

**Exemplo: usando uma instância personalizada do Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### Instalar o servidor de relatórios e usar um banco de dados de relatórios existente em um computador local

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Exemplo: usando uma instância personalizada do Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Instalar o servidor de relatórios usando um banco de dados de relatórios existente em um computador remoto

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /REPORTING _SERVER
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):

- /REPORTING _SERVER
- */REPORTING _ADMINACCOUNT*
- /REPORTING _WEBSITE_NAME
- /REPORTING _WEBSITE_PORT
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Exemplo: usando uma instância personalizada do Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Instalar o banco de dados de relatórios no mesmo computador que o servidor de relatório

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /REPORTING _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):

- /DB_PREDEPLOY_REPORTING
- */REPORTING _DB_CUSTOM_SQLINSTANCE*
- /REPORTING _DB_NAME
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Exemplo: usando uma instância personalizada do Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Instalar o banco de dados de relatórios em um computador diferente do que o servidor de relatório

Para usar a instância padrão do Microsoft SQL Server, use os seguintes parâmetros (diferença da instância personalizada em *itálico*):

- /DB_PREDEPLOY_REPORTING
- /REPORTING _DB_SQLINSTANCE_USE_DEFAULT
- /REPORTING _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Para usar uma instância personalizada do Microsoft SQL Server, use estes parâmetros (diferença da instância padrão em *itálico*):

- /DB_PREDEPLOY_REPORTING
- /REPORTING _DB_CUSTOM_SQLINSTANCE
- /REPORTING _DB_NAME
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Exemplo: usando uma instância personalizada do Microsoft SQL Server:**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Definições de parâmetro

#### Parâmetros gerais

| Parâmetro | Informações |
|--|--|
| /QUIET | Especifica a instalação silenciosa. |
| /UNINSTALL | Especifica uma desinstalação. |
| /LAYOUT | Especifica a ação de layout. Isso extrai os arquivos MSIs e script para uma pasta sem realmente instalar o produto. Nenhum valor é esperado. |
| /LAYOUTDIR | Especifica o diretório de layout. Usa uma cadeia de caracteres. Exemplo de uso: **/LAYOUTDIR = "servidor de virtualização C:\\Application"** |
| /INSTALLDIR | Especifica o diretório de instalação. Usa uma cadeia de caracteres. Exemplo de uso: **/installdir = "C:\\Arquivos Files\\Application Virtualization\\Server"** |
| /MUOPTIN | Habilita o Microsoft Update. Nenhum valor é esperado. |
| /ACCEPTEULA | Aceita o contrato de licença. Isso é necessário para uma instalação automática. Exemplo de uso: **/AcceptEula** ou **/ACCEPTEULA = 1** |

#### Parâmetros de instalação do servidor de gerenciamento

|Parâmetro |Informações |
|--|--|
| /MANAGEMENT_SERVER | Especifica que o servidor de gerenciamento será instalado. Nenhum valor é esperado |
| /MANAGEMENT_ADMINACCOUNT | Especifica a conta à qual o acesso de administrador será permitido para o servidor de gerenciamento. Pode ser uma conta de usuário ou um grupo. Exemplo de uso: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**. Se **/MANAGEMENT_SERVER** não for especificado, isso será ignorado. |
| /MANAGEMENT_WEBSITE_NAME | Especifica o nome do site que será criado para o serviço de gerenciamento. Exemplo de uso: **/MANAGEMENT_WEBSITE_NAME = "serviço de gerenciamento do Microsoft App-V"** |
| MANAGEMENT_WEBSITE_PORT | Especifica o número da porta que será usada pelo serviço de gerenciamento que será usado. Exemplo de uso: **/MANAGEMENT_WEBSITE_PORT = 82** |

#### Parâmetros para o banco de dados do servidor de gerenciamento

| Parâmetro | Informações |
|--|--|
| /DB_PREDEPLOY_MANAGEMENT | Especifica que o banco de dados de gerenciamento será instalado. Você deve ter permissões de banco de dados suficientes para concluir a instalação. Nenhum valor é esperado. |
| /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Indica que a instância SQL padrão deve ser usada. Nenhum valor é esperado. |
| /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Especifica o nome da instância SQL personalizada que deve ser usada para criar um novo banco de dados. Exemplo de uso: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"**. Se **/DB_PREDEPLOY_MANAGEMENT** não for especificado, isso será ignorado. |
| /MANAGEMENT_DB_NAME | Especifica o nome do novo banco de dados de gerenciamento que deve ser criado. Exemplo de uso: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Se **/DB_PREDEPLOY_MANAGEMENT** não for especificado, isso será ignorado. |
| /MANAGEMENT_SERVER_MACHINE_USE_LOCAL | Indica se o servidor de gerenciamento que vai acessar o banco de dados está instalado no servidor local. Parâmetro de opção; portanto, nenhum valor é esperado. |
| /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT | Especifica a conta de máquina do computador remoto em que o servidor de gerenciamento será instalado. Exemplo de uso: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"** |
| /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT | Indica a conta de administrador que será usada para instalar o servidor de gerenciamento. Exemplo de uso: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Parâmetros para instalar o Publishing Server

| Parâmetro | Informações |
|--|--|
| /PUBLISHING_SERVER | Especifica que o servidor de publicação será instalado. Nenhum valor é esperado. |
| /PUBLISHING_MGT_SERVER | Especifica a URL para o serviço de gerenciamento ao qual o servidor de publicação será conectado. Exemplo de uso: **http:// &lt; Management Server Name &gt; : número &lt; &gt; de porta do servidor de gerenciamento**. Se **/PUBLISHING_SERVER** não for usado, este parâmetro será ignorado. |
| /PUBLISHING_WEBSITE_NAME | Especifica o nome do site que será criado para o serviço de publicação. Exemplo de uso: **/PUBLISHING_WEBSITE_NAME = "serviço Microsoft App-V Publishing"** |
| /PUBLISHING_WEBSITE_PORT | Especifica o número da porta usada pelo serviço de publicação. Exemplo de uso: **/PUBLISHING_WEBSITE_PORT = 83** |

#### Parâmetros do servidor de relatório

| Parâmetro | Informações |
|--|--|
| /REPORTING_SERVER | Especifica que o servidor de relatórios será instalado. Nenhum valor é esperado. |
| /REPORTING_WEBSITE_NAME | Especifica o nome do site que será criado para o serviço de relatório. Exemplo de uso: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"** |
| /REPORTING_WEBSITE_PORT | Especifica o número da porta que o serviço de relatórios vai usar. Exemplo de uso: **/REPORTING_WEBSITE_PORT = 82** |

#### Parâmetros para usar um banco de dados do servidor de relatórios existente

| Parâmetro | Informações |
|--|--|
| /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL | Indica que o Microsoft SQL Server está instalado no servidor local. Parâmetro de opção; portanto, nenhum valor é esperado. |
| /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME | Especifica o nome do computador remoto no qual o SQL Server está instalado. Usa uma cadeia de caracteres. Exemplo de uso: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ _DB_SQLINSTANCE_USE_DEFAULT DE RELATÓRIO | Indica que a instância SQL padrão deve ser usada. Parâmetro de opção; portanto, nenhum valor é esperado. |
| /EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE | Especifica o nome da instância SQL personalizada que deve ser usada. Usa uma cadeia de caracteres. Exemplo de uso: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"** |
| /EXISTING_ _DB_NAME DE RELATÓRIO | Especifica o nome do banco de dados de relatórios existente que deve ser usado. Usa uma cadeia de caracteres. Exemplo de uso: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"** |

#### Parâmetros para instalar o banco de dados do servidor de relatório

| Parâmetro | Informações |
|--|--|
| /DB_PREDEPLOY_REPORTING | Especifica que o banco de dados de relatórios será instalado. As permissões do DBA são necessárias para esta instalação. Nenhum valor é esperado. |
| /REPORTING_DB_SQLINSTANCE_USE_DEFAULT | Especifica o nome da instância SQL personalizada que deve ser usada. Usa uma cadeia de caracteres. Exemplo de uso: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "MySqlServer"** |
| /REPORTING_DB_NAME | Especifica o nome do novo banco de dados de relatórios que deve ser criado. Usa uma cadeia de caracteres. Exemplo de uso: **/REPORTING_DB_NAME = "AppVMgmtDB"** |
| /REPORTING_SERVER_MACHINE_USE_LOCAL | Indica que o servidor de relatórios que vai acessar o banco de dados está instalado no servidor local. Parâmetro de opção; portanto, nenhum valor é esperado. |
| /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT | Especifica a conta de máquina do computador remoto em que o servidor de relatórios será instalado. Usa uma cadeia de caracteres. Exemplo de uso: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\computername"** |
| /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT | Indica a conta de administrador que será usada para instalar o servidor de relatórios do App-V. Usa uma cadeia de caracteres. Exemplo de uso: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Parâmetros para usar um banco de dados existente do servidor de gerenciamento

| Parâmetro | Informações |
|--|--|
| /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL | Indica que o SQL Server está instalado no servidor local. Parâmetro de opção; portanto, nenhum valor é esperado. Se **/DB_PREDEPLOY_MANAGEMENT** for especificado, será ignorado. |
| /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME | Especifica o nome do computador remoto no qual o SQL Server está instalado. Usa uma cadeia de caracteres. Exemplo de uso: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Indica que a instância SQL padrão deve ser usada. Parâmetro de opção; portanto, nenhum valor é esperado. Se **/DB_PREDEPLOY_MANAGEMENT** for especificado, será ignorado. |
| /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Especifica o nome da instância SQL personalizada que será usada. Exemplo de uso **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**. Se **/DB_PREDEPLOY_MANAGEMENT** for especificado, será ignorado. |
| /EXISTING_MANAGEMENT_DB_NAME | Especifica o nome do banco de dados de gerenciamento existente que deve ser usado. Exemplo de uso: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Se **/DB_PREDEPLOY_MANAGEMENT** for especificado, será ignorado. |

Tem um problema com o App-V? Use o [Fórum do TechNet do App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Tópicos relacionados

[Implantação do servidor App-V 5.1](deploying-the-app-v-51-server.md)
